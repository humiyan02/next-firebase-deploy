https://test-next-humiyan02.web.app/

# デプロイ方法
1. firebase initでhostingを選ぶ
2. "public": "out",に設定する。
```
{
  "hosting": {
    "public": "out",
    "ignore": [
      "firebase.json",
      "**/.*",
      "**/node_modules/**"
    ],
    "rewrites": [
      {
        "source": "**",
        "destination": "/index.html"
      }
    ]
  }
}
```
3. yarn build && yarn export するとoutディレクトリが出てくる。
4. firebase serveで確かめる
5. firebase deploy --only hostingする
  