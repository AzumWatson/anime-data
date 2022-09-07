# anime-data

新番表数据 随时更新

抓取各大（hazx新番简介，bgm.tv）的数据并整合，由于是脚本整合，译名等部分字符存在差异导致无法完美进行匹配，造成数据缺失，后续可能会手动再处理一边。

## 如何使用

直接get请求 https://raw.githubusercontent.com/AzumWatson/anime-data/main/data.json

## API 回应标准结构

{
    "weekday": {
        "id": 1,
        "cn": "周一"
    },
    "items": [{
        "name": "森林里的熊先生、冬眠中。",
        "time": "00:00",
        "name_jp": "森のくまさん、冬眠中。",
        "id": 342673,
        "air_date": "2022-07-03",
        "img": {
                "large": "http://lain.bgm.tv/pic/cover/l/75/b3/342673_866b8.jpg",
                "common": "http://lain.bgm.tv/pic/cover/c/75/b3/342673_866b8.jpg",
                "medium": "http://lain.bgm.tv/pic/cover/m/75/b3/342673_866b8.jpg",
                "small": "http://lain.bgm.tv/pic/cover/s/75/b3/342673_866b8.jpg",
                "grid": "http://lain.bgm.tv/pic/cover/g/75/b3/342673_866b8.jpg"
         }
    },{
        "name": "Love Live 爱与演唱会!超级明星!! 第二季",
        "time": "17:30"
    }]
}

| 属性   | 说明               | 类别   | 
| ---- | ------------------ | ------ | 
| weekday.id    | 类似下标吧但是是 1 | int  |
| weekday.cn    | 一周中的哪一天例如 周一 | string  |
| items    | 里面存放着一天中所有要更新的番剧 | array  |

{
    "name": "森林里的熊先生、冬眠中。",
    "time": "00:00",
    "name_jp": "森のくまさん、冬眠中。",
    "id": 342673,
    "air_date": "2022-07-03",
    "img": {
            "large": "http://lain.bgm.tv/pic/cover/l/75/b3/342673_866b8.jpg",
            "common": "http://lain.bgm.tv/pic/cover/c/75/b3/342673_866b8.jpg",
            "medium": "http://lain.bgm.tv/pic/cover/m/75/b3/342673_866b8.jpg",
            "small": "http://lain.bgm.tv/pic/cover/s/75/b3/342673_866b8.jpg",
            "grid": "http://lain.bgm.tv/pic/cover/g/75/b3/342673_866b8.jpg"
     }
}

| 属性   | 说明               | 类别   | 
| ---- | ------------------ | ------ | 
| name    | 番剧名称 | string  |
| time    | 更新时间 | string  |
| name_jp    | 番剧日文名 | string  |
| id    | bgm.tv 的 id | int  |
| air_date    | 番剧放送日期(首播) | string  |
| img    | 番剧缩略图 | object  |

{
    "name": "Love Live 爱与演唱会!超级明星!! 第二季",
    "time": "17:30"
}

有一些番剧回像上面的一样存在数据缺失，这是正常的，后续可能会补上。

最后更新:2022年9月7日21点17分
