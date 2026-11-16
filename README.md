# 海南島 五萬分一 · 三套歷史地形圖对照

**在线浏览：** <https://ewlaker.github.io/hainan5w-ALL/>

---

## 这是什么

一页把**三套不同版次的海南島五万分一**叠在一起对照的 Leaflet 页面：

| 套 | 版本 | 幅数 | 瓦片仓库 |
|---|---|---|---|
| A | 中研院 · 廣東陸地測量局（民 27/37） | 101 | [hainan5w-A](https://github.com/EWlaker/hainan5w-A) |
| B | 東北大学外邦図 · 日本陸地測量部 1940 | 96 | [hainan5w-B](https://github.com/EWlaker/hainan5w-B) |
| C | 中研院 RCHSS · 廣東陸地測量局 | 101 | [hainan5w-C](https://github.com/EWlaker/hainan5w-C) |

三套格网已统一到同一参考系（13.18′×9.75′ 名义分幅），**同名图可直接叠合**看两版差异。
每格常显「图名 + 图号」，缩放到 z10 以上出现；虚线框表示只有部分套收录
（外邦図在原档案里缺 4 幅）。

## 页面功能

- 勾选 A / B / C 任意叠加，透明度滑块统一调节
- **底图切换**：无（深色）/ 天地图·矢量 / 天地图·影像 / 天地图·地形 / OSM
- 图幅接合表可开关，点格子看三套各自编号与行列
- URL 参数直接定位：`?z=11&lat=19.2&lon=109.7&base=tdt_img`

## 目录结构

```
index.html            页面本体（单文件，依赖 CDN 上的 Leaflet）
sheets_index.geojson  图幅接合表（101 格，含三套图号）
404.html
.nojekyll             关掉 Jekyll，加快 Pages 构建
```

瓦片不在本仓库，来自上面三个仓库（`SITES` 常量里配置）。

## 改动

改 `index.html` 里的 `SITES` 就能换瓦片来源；`TDT_KEY` 是天地图的 key，
建议换成自己申请的（<https://console.tianditu.gov.cn> 免费）。

图上坐标是名义分幅（民国图廓按 WGS84 表达），适合浏览对照，不作测绘控制底图使用。
