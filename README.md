# chromium_learning
## 源码获取
1. cmd中设置代理
```cmd
set http_proxy=http://127.0.0.1:10809
set https_proxy=http://127.0.0.1:10809
```
2. 其他配置教程
<https://chromium.googlesource.com/chromium/src/+/main/docs/windows_build_instructions.md>

3. 拉取chromium源码

   ```cmd
   fetch chromium
   
   # 不要历史数据，节省时间
   fetch --no-history chromium
   ```

4. 编译项目

   ```cmd
   # 构建visual studio工程
   cd src
   gn gen out\Default --ide=vs2022 --args="is_component_build=true is_debug=true"
   
   # 编译chrome
   ninja -C out/default chrome
   ```

   

