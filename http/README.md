

## 跟随跳转

```
curl -L http://curl.haxx.se
```

## 表单提交

```
curl -d log=aaaa http://blog.51yip.com/wp-login.php
```

## 伪造来源地址（Referer fake）

```
curl -e http://moooofly.com http://blog.51yip.com/wp-login.php
```

## 分段下载

```
curl -r 0-100 -o img.part1 http://blog.51yip.com/wp-content/uploads/2010/09/compare_varnish.jpg
curl -r 100-200 -o img.part2 http://blog.51yip.com/wp-content/uploads/2010/09/compare_varnish.jpg
curl -r 200- -o img.part3 http://blog.51yip.com/wp-content/uploads/2010/09/compare_varnish.jpg
```

合并

```
ls | grep part | xargs du -sh
cat img.part* > img.jpg
```
