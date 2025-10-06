# RetailCRM Transport API Schema

[![License](https://img.shields.io/github/license/integratop/retailcrm-transport-api-schema)](https://opensource.org/licenses/MIT)
[![npm version](https://img.shields.io/npm/v/@integratop/retailcrm-transport-api-schema.svg)](https://www.npmjs.com/package/@integratop/retailcrm-transport-api-schema)

OpenAPI схема для REST Transport API CRM системы RetailCRM. Библиотека предоставляет описание Transport API для работы с каналами, файлами, шаблонами и сообщениями RetailCRM.

## Установка

```bash
npm install @integratop/retailcrm-transport-api-schema --save-dev
```

```bash
yarn add @integratop/retailcrm-transport-api-schema --save-dev
```

```bash
pnpm add @integratop/retailcrm-transport-api-schema --save-dev
```

## Использование

### Как инструмент командной строки

Библиотеку можно использовать как CLI инструмент для получения OpenAPI схемы в stdout:

```bash
# Получить схему в формате JSON
npx @integratop/retailcrm-transport-api-schema

# Получить схему в формате YAML
npx @integratop/retailcrm-transport-api-schema --yaml

# Сохранить схему в файл
npx @integratop/retailcrm-transport-api-schema > transport-api-schema.json

# Использовать с jq для фильтрации
npx @integratop/retailcrm-transport-api-schema | jq '.paths["/templates"]'
```

### Импорт JSON схемы

```typescript
import schema from "@integratop/retailcrm-transport-api-schema/schemas/schema.json" with { type: "json" };

console.log(schema.info);
```

### Импорт TypeScript объекта

```typescript
import { schema } from '@integratop/retailcrm-transport-api-schema';

console.log(schema.info);
```

## Разработка

### Сборка проекта

```bash
# Установка зависимостей
pnpm install

# Запуск тестов
pnpm test

# Сборка проекта
pnpm build
```

### Обновление схемы

Для обновления схемы из внешнего источника:

```bash
# Установите переменную окружения с URL схемы
export RETAIL_CRM_TRANSPORT_API_SCHEMA_URL="https://ваш-url-схемы/schema.json"

# Загрузка и обновление схемы
pnpm download-schema
pnpm build
```

## Лицензия

MIT License - смотрите файл [LICENSE](LICENSE) для подробностей.

## Версионирование

Проект использует [Semantic Versioning](https://semver.org/).

## Безопасность

Если вы обнаружили уязвимость безопасности, пожалуйста, сообщите нам об этом.

## Поддержка

Если у вас есть вопросы или предложения, создайте issue в [GitHub репозитории](https://github.com/integratop/retailcrm-transport-api-effect/issues).

---

**Примечание**: Эта библиотека содержит только схему OpenAPI и не предоставляет реализацию клиента. Для работы с API RetailCRM необходимо реализовать клиент на основе предоставленной схемы.
