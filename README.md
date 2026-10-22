# 手机网页应用测试

公网地址：https://bme-coder.github.io/links-aiapp-web-demo/

这是一个无需安装依赖的手机网页应用。内容保存在当前设备的浏览器里；不同设备之间不会同步。

## 本地预览

```sh
cd /Users/zhangchunwei/ai_project/Links_aiapp/web-demo
python3 -m http.server 4173 --bind 0.0.0.0
```

Mac 上打开 http://127.0.0.1:4173/。同一 Wi-Fi 下的 iPhone 可以通过 Mac 的局域网 IP 访问 4173 端口。公网地址不依赖 Mac 保持开机。

## 修改后发布

远程连接 Mac 后进入本目录，修改页面文件，再运行：

```sh
git add index.html manifest.webmanifest sw.js README.md .gitignore .nojekyll
git commit -m "Update web app"
git push origin main
```

GitHub Pages 会自动发布 `main` 分支。通常等待几分钟，随后在 iPhone Safari 刷新公网地址。Safari 的分享菜单中可以选择“添加到主屏幕”，以后从主屏幕打开。

仓库：https://github.com/Bme-coder/links-aiapp-web-demo 。免费公开托管，源码也公开。不要把密码、令牌或私人数据写入这个仓库。
