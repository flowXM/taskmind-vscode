# Intelligent Tasks Manager (VS Code Extension)

Этот плагин для Visual Studio Code помогает вам управлять комментариями типа TODO, FIXME, BUG, NOTE, визуализируя их в удобной панели.

## 📦 Установка

1. Склонируйте репозиторий:
```
git clone <repo-url>
```

2. Установите зависимости:
```
npm install
```

3. Сборка плагина:
```
npm run compile
```

4. Упакуйте в `.vsix` файл:
```
npx vsce package
```

5. Установите плагин в VS Code:
```
code --install-extension <путь к vsix>
```

## 🤖 ИИ-интеграция

Плагин поддерживает интеграцию с локальными LLM через Ollama:

1. Установите [Ollama](https://ollama.ai/)
2. Скачайте модель:
```bash
ollama pull codellama
```

## 🚀 Использование

- Откройте панель **Intelligent Tasks** в дереве проводника.
- Сканируйте рабочее пространство с помощью команды `Сканировать рабочее пространство`.
- Отмечайте задачи как выполненные.

## 🔧 Настройки

В `settings.json` вы можете указать теги для отслеживания:
```json
"intelligentTasks.todoPatterns": ["TODO", "FIXME", "BUG", "NOTE"]
```
а также настройки ИИ:
```json
"intelligentTasks.ollamaUrl": "http://localhost:11434",
"intelligentTasks.aiModel": "codellama"
"intelligentTasks.contextLines": 15
```
