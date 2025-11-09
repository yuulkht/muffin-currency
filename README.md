# muffin-currency

### Создание чарта
```
helm create muffin-currency-chart
```

### Тестово посмотреть на файлы

```
helm install --dry-run test-release ./muffin-currency-chart
```

### Установить релиз
```
helm install muffin-currency-release ./muffin-currency-chart
```

### Установка с переопределениеем значений
```
helm install muffin-currency-release ./muffin-currency \
  --set replicaCount=3 \
  --set image.tag="1.1.0" \
  --set service.port=8084
```

### Список всех релизов
```
helm list
```

### Статус конкретного релиза
```
helm status muffin-currency-release
```

### История релиза
```
helm history muffin-currency-release
```

### Получить значения релиза
```
helm get values muffin-currency-release
```

###  Обновление с новыми values
```
helm upgrade muffin-currency-release ./muffin-currency-chart \
  --set replicaCount=4
```

### Обновление с новым файлом
```
helm upgrade muffin-currency-release ./muffin-currency-chart \
  -f values-production.yaml
```

### Просмотр истории
```
helm history muffin-currency-release
```

### Откат к предыдущей версии
```
helm rollback muffin-currency-release 1
```

### Откат к конкретной версии
```
helm rollback muffin-currency-release 3
```

### Удаление
```
helm uninstall muffin-currency-release
```
