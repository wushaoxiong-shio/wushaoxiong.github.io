# 个人博客仓库
- 从 ArthurChiao 所属仓库克隆
- 原仓库地址：https://github.com/ArthurChiao/arthurchiao.github.io

# 构建
- 安装依赖
apt install ruby-full build-essential zlib1g-dev -y

echo 'export GEM_HOME="$HOME/gems"' >> ~/.zshrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc

- 项目构建
git clone https://github.com/wushaoxiong-shio/wushaoxiong.github.io.git

cd wushaoxiong.github.io
gem install jekyll bundler
bundle install
bundle exec jekyll build --incremental

- 打包部署
cp -rf _site/* /nignx-dir/

- 本地预览
bundle exec jekyll serve --incremental