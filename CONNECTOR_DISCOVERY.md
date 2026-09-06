# Fishbowl Inventory Connector — Connector Discovery

**Category:** C46. Warehouse & 3PL Logistics Management  
**Vendor:** Fishbowl Inventory  
**Official Website:** https://www.fishbowlinventory.com

## 1. Официальный API
- **Базовый URL API:** `https://<fishbowl-server>:23274/api`
- **Поддерживаемая модель авторизации:** Fishbowl Server Token / App Key Login

## 2. Архитектура сущностей
- Ключевые ресурсы платформы Fishbowl Inventory:
  - товары/детали (/parts)
  - складские остатки (/inventory)
  - заказы на закупку (/pos)
  - заказы на продажу (/sos)

## 3. Требования к отказоустойчивости и безопасности
- Соблюдение вендорных лимитов запросов (Rate Limiting) с экспоненциальной задержкой.
- Строгая валидация Pydantic-схем на входе и выходе каждого запроса.
- Тестовая точка проверки подключения: `GET /api/inventory/status`.
