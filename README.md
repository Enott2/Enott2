# Проверьте наличие существующих ключей
ls ~/.ssh

# Если нет, сгенерируйте новый (замените на свою почту)
ssh-keygen -t ed25519 -C "your_email@example.com"

# Запустите ssh-agent и добавьте ключ
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

# Просмотрите публичный ключ и скопируйте его
cat ~/.ssh/id_ed25519.pub
