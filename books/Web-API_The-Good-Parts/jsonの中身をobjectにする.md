# jsonの中身をobjectにする

APIのレスポンスに

- 配列をそのまま返す方法
- レスポンス全体をオブジェクトにして返す方法

がある。

配列をそのまま返す
```JSON
[
  {
    "id" : 1,
    "name" : "cureseven",
    "profileIcon" : "http://image.example.com/profile/1.png",
    ...
  },
  {
    "id" : 2,
    "name" : "cureeight",
    "profileIcon" : "http://image.example.com/profile/2.png",
    ...
  },
  ...
]
```

オブジェクトで包む
```JSON
{
  "friends" : [
    {
      "id" : 1,
      "name" : "cureseven",
      "profileIcon" : "http://image.example.com/profile/1.png",
      ...
    },
    {
      "id" : 2,
      "name" : "cureeight",
      "profileIcon" : "http://image.example.com/profile/2.png",
      ...
    },
    ...
  ]
}
```

## オブジェクトで包むことで得られるいいこと

- レスポンスデータが何を示しているものかわかりやすくなる
- レスポンスデータをオブジェクトに統一できる
- セキュリティ上のリスクを避けられる
  - JSONインジェクション対策。javascriptで `{}`の中はjavascriptの構文が期待される
