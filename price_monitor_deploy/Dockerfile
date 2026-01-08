# 使用官方 Python 轻量级镜像
FROM python:3.9-slim

# 设置工作目录
WORKDIR /app

# 复制依赖文件
COPY requirements.txt .

# 安装依赖
RUN pip install --no-cache-dir -r requirements.txt

# 复制项目代码
COPY . .

# 暴露端口 5000
EXPOSE 5000

# 启动命令：强制监听 5000 端口
CMD gunicorn --bind 0.0.0.0:5000 app:app