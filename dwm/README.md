# Dwm | *dynamic window manager*

- Dwm 依赖于 X服务器
- 安装 Dwm `sudo make install`


#### 添加功能
1. 自启动脚本
2. Grid布局
3. 悬浮终端

# 源码解析
## 文件结构

### 创建布局
1. 将函数定义添加到 dwm.c **`static void "布局名" (Monitor *m);`**
2. 书写函数内容
``` cpp
int layout(Monitor *m) {
	unsigned int i, n; // i:	n:桌面窗口总数
	unsigned int cx, cy, cw, ch;
	unsigned int cols, rows;
	Client* c;

	// 获取窗口数
	for (n = 0, c = nexttiled(m->clients); c = nexttiled(m->clients), n++);
}
```
