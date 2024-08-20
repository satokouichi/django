# ベースイメージを指定
FROM python:3.9

# 作業ディレクトリを作成
WORKDIR /var/www/vhosts

# 必要なパッケージをインストール
COPY requirements.txt /var/www/vhosts/
RUN pip install --no-cache-dir -r requirements.txt

# アプリケーションコードをコピー
COPY . /var/www/vhosts/

# ポートを開放
EXPOSE 80

# Gunicornを起動
CMD ["gunicorn", "wsgi:application", "--bind", "0.0.0.0:80"]
