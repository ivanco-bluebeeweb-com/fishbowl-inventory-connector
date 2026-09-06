# Fishbowl Inventory Connector — Auth & Credentials Standard

**Compliance:** AUTH_AND_CREDENTIALS_STANDARD.md (B1–B10)

## Схема аутентификации
- **Метод:** Fishbowl Server Token / App Key Login
- **Хранение:** Секреты сохраняются изолированно в хранилище секретов платформы Imperal.
- **Валидация:** При сохранении ключа выполняется тестовый запрос `GET /api/inventory/status`.
- **Отключение:** Удаление локальных ключей без воздействия на аккаунт вендора.
