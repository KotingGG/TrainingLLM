# TrainingLLM

Данный репозиторий используется исключительно для обучения. Главный объект обучения - **LLM (Large Language Model)**. 
Обучение происходит параллельно с изучением [бесплатного курса](https://stepik.org/course/215591/info) на площадке **Stepik**. 

## Предварительные требования

1. **Для запуска локального LLM: Ollama** с [официального сайта](https://ollama.ai/).
2. **Необходимая LLM-модель** через Ollama. Для этого проекта используется `mistral 7B` (базовый):
```bash
ollama run mistral
```
Минимальные требования для запуска: 8 GB ОЗУ.

3. **Фреймфорки, библиотеки:** 
- Используются до жути много библиотек, ведь тестируются разные методы. Самые популярные:
```bash
pip install langchain
```
```bash
pip install langchain_ollama
```
```bash
pip install chainlit
```
```bash
pip install langchain_community
```
```bash
pip install langchain_core
```
```bash
pip install langgraph
```
```bash
pip install pydantic
```
```bash
pip install fastapi[standard]
```

Некоторые фреймворки могут не использоваться в основной части.

## Запуск веб-страницы с LLM
Для начала необходимо установить саму Ollama. Для этого установим её с офицального сайта `https://ollama.com/`. 
Установить локальную большую языковую модель
```bash
ollama run mistral
```
Через время после установки, можно потестировать её в терминале. Чтобы выйти, введите `/bye`.

Перед запуском убедитесь, что у вас запущен Ollama:
```bash
# Запустить Ollama сервер (в отдельном терминале)
ollama serve

# Запустить Chainlit веб-страницу (в отдельном терминале)
chainlit run main/ChatProfileWeb.py -w
```
После переходим на `http://127.0.0.1:8000`

## Запуск API (в данный момент тестовый)
```bash
fastapi dev API    
```  
После переходим на `http://127.0.0.1:8000`
Встроенная документация: `http://127.0.0.1:8000/docs#/`
