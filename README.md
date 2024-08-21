# 起動・削除
docker-compose down --rmi all --volumes --remove-orphans
docker-compose build --no-cache
docker-compose up -d

# postgresログインとDB表示
psql -U user -d django
\l

# djangoインストール

# 所有権者変更
chown -R 1000:1000 database/seeders/*

# キャッシュクリア

# node + npm インストール
apt update
apt install -y nodejs npm
npm install n -g
n lts
apt purge nodejs npm
docker exec 〜 (再ログイン)
node -v
npm -v
npm install

# npm 再インストール
npm cache clean -f
rm -rf node_modules
npm install