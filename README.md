# Ansible role for install ssh private and public keys

## Переменные

### Описание

user_name - имя пользователя, которого необходимо добавить
ssh_private_key - приватный ключ пользователя
ssh_public_key - публичный ключ пользователя

### Значения по-умолчанию

```YAML
---
user_name: "hi_user"
ssh_private_key: |
  -- START PRIVATE --
  hello
  --  END PRIVATE  --
ssh_public_key: "hi_user"
```

## Установка

Добавить в файл requirements.yml
```
- src: https://github.com/rzsvet/ansible-role-ssh_install_key.git
```
Перед выполнением запустить
```
ansible-galaxy install -r requirements.yml
```

## Применение

Данная роль используется для добавления пользователю user_name приватных и публичных ключей описанных в переменных ssh_private_key и ssh_public_key
Для сохранности ключей их лучше вего прописать в group_vars в переменных ssh_public_key, ssh_private_key

## Примечание

Данная роль тестовая и врядли пригодится для использования в реальных проектах. Старайтесь не использовать сторонние роли, чтобы случайно не загрузить вредный код.