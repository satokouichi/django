ARG PYTHON_VERSION
FROM python:${PYTHON_VERSION}

# 作業ディレクトリを作成
WORKDIR /var/www/vhosts

# 必要なパッケージをインストール
COPY requirements.txt /var/www/vhosts/
RUN pip install --no-cache-dir -r requirements.txt

# アプリケーションコードをコピー
COPY . /var/www/vhosts/

# ポートを開放
EXPOSE 80

# コンテナ起動時にDjangoプロジェクトを作成するためのエントリポイントスクリプトを実行
CMD ["sh", "-c", "django-admin startproject mysite . && gunicorn mysite.wsgi:application --bind 0.0.0.0:80"]