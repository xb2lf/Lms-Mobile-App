# Lms-Mobile-App

Lms-Mobile-App 是一个完整的学习管理系统（LMS），包含移动端应用、后台管理系统和后端服务。移动端应用基于 TypeScript 和 React Native 并依托 Expo 框架开发，后台管理系统使用 React 构建，后端服务则基于 Express.js 实现。项目借助多个第三方服务来完成接口、验证和数据库等功能，包括 Upstash、VdoCipher、Cloudinary、Stripe 和 MongoDB。

## 项目结构

- admin：后台管理系统，使用 React 构建，用于管理学习系统的各类信息。
- server：后端服务，基于 Express.js 实现，处理业务逻辑和与数据库交互。
- client：移动端应用，使用 TypeScript 和 React Native 并依托 Expo 框架开发，为用户提供学习体验。

## 第三方服务支持

1. [Upstash]: (https://upstash.com)

- 用于缓存和消息队列，提升系统性能和响应速度。

2. [VdoCipher]: (https://vdocipher.com)

- 提供视频加密和播放服务，确保学习视频的安全性和流畅播放。

3. [Cloudinary]: (https://cloudinary.com)

- 用于管理和优化图像、视频等媒体资源。

4. [Cloudinary]: (https://stripe.com)

- 集成支付功能，方便用户进行课程购买等操作

5. [MongoDB]: (https://www.mongodb.com)

- 作为主要的数据库，存储学习系统的各类数据，如用户信息、课程信息等。

## 子项目说明

### admin（后台管理系统）

#### 项目简介

该子项目是基于 React 构建的后台管理系统，用于管理学习系统的各种信息，如用户管理、课程管理、订单管理等。

#### 环境要求

- Node.js (v14.x 及以上)

- npm (v6.x 及以上)

#### 安装与 运行

1. 进入 admin 目录

```bash
  cd admin
```

2. 安装依赖

```bash
  npm install
```

3. 启动开发服务器

```bash
  npm run dev
```

4. 配置

在 admin/.env 文件中配置相关环境变量，例如：

```plaintext
  REACT_APP_API_BASE_URL=http://localhost:3001/api
```

### server（后端服务）

#### 项目简介

基于 Express.js 的后端服务，负责处理业务逻辑和与数据库交互，为前端提供接口服务。

#### 环境要求

- Node.js (v14.x 及以上)

- npm (v6.x 及以上)

#### 安装与 运行

1. 进入 server 目录

```bash
  cd server
```

2. 安装依赖

```bash
  npm install
```

3. 启动开发服务器

```bash
  npm run dev
```

4. 配置

在 server/.env 文件中配置相关环境变量，例如：

```plaintext
  PORT=3001
  MONGODB_URI=mongodb+srv://your_username:your_password@your_cluster.mongodb.net/your_database
  UPSTASH_REDIS_URL=your_upstash_redis_url
  VDOCIPHER_API_KEY=your_vdocipher_api_key
  CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
  CLOUDINARY_API_KEY=your_cloudinary_api_key
  CLOUDINARY_API_SECRET=your_cloudinary_api_secret
  STRIPE_SECRET_KEY=your_stripe_secret_key
```

### client（移动端应用）

#### 项目简介

使用 TypeScript 和 React Native 并依托 Expo 框架开发的移动端应用，为用户提供学习体验，包括课程浏览、学习、支付等功能。

#### 环境要求

- Node.js (v14.x 及以上)

- npm (v6.x 及以上)

- Expo

#### 安装与 运行

1. 进入 client 目录

```bash
  cd client
```

2. 安装依赖

```bash
  npm install
```

3. 启动开发服务器

```bash
  npx exo start
```

4. 配置

在 client/.env 文件中配置相关环境变量，例如：

```plaintext
  API_BASE_URL=http://localhost:3001/api
```