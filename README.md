# TravelSystem

旅游系统前后端分离项目，仓库由两个子模块组成：
- `travelsystem_backend`：Django + Django Ninja 后端服务
- `travelsystem_frontend`：Vue 3 前端应用

## 技术栈

### 后端（travelsystem_backend）
- Django 5.x
- Django Ninja（API 框架）
- Django Channels + Redis（实时通信）
- JWT（`ninja_jwt`）
- Captcha（验证码）
- SQLite（开发环境默认）

### 前端（travelsystem_frontend）
- Vue 3 + Vite
- Vue Router
- Element Plus
- Axios

## 快速启动

### 1. 拉取子模块
```bash
git submodule update --init --recursive
```

### 2. 启动后端
```bash
cd travelsystem_backend
python manage.py makemigrations
python manage.py migrate
python .\manage.py ingest_list
python ./manage.py runserver
```

常用依赖（按需安装）：
```bash
pip install django-ninja django-cors-headers Pillow django-simple-captcha redis
```

### 3. 启动前端
```bash
cd travelsystem_frontend
npm install
npm run dev
```

## 说明
- 本仓库为聚合仓（mono-repo 风格），前后端代码位于各自子模块中。
- 建议先完成后端环境配置，再启动前端进行联调。
