# Отчёт по лабораторной работе №2

**Студент:** Maksim Alehanov
**Группа:** ИУ8-25
**Тема:** Изучение систем контроля версий на примере Git

---

## 1. Цель работы

Освоить базовую работу с системой контроля версий Git и сервисом GitHub:
настройку, создание репозитория, фиксацию изменений и работу с ветками.

## 2. Выполнение

### 2.1. Настройка окружения

```sh
export GITHUB_USERNAME=sasun1100
export GITHUB_EMAIL=maks4182@gmail.com
export GITHUB_TOKEN=<токен с правами repo>
```

Настроен доступ через hub:

```sh
mkdir ~/.config
cat > ~/.config/hub <<EOF
github.com:
- user: sasun1100
  oauth_token: ${GITHUB_TOKEN}
  protocol: https
EOF
git config --global hub.protocol https
```

### 2.2. Настройка Git

```sh
git config --global user.name "sasun1100"
git config --global user.email "maks4182@gmail.com"
```

### 2.3. Создание репозитория

Создан публичный репозиторий **lab02** с лицензией MIT.

```sh
git clone https://github.com/sasun1100/lab02
cd lab02
```

### 2.4. Базовые операции

```sh
# изменения
edit README.md
git status
git add README.md
git commit -m "update readme"
git push origin master

# работа с ветками
git branch feature
git checkout feature
git commit -am "work in branch"
git checkout master
git merge feature
git log --oneline --graph
```

## 3. Результаты

- Настроены Git и доступ к GitHub через токен.
- Создан репозиторий lab02 с лицензией MIT.
- Освоены команды фиксации изменений, ветвления и слияния.
