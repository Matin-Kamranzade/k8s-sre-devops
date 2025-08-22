# k8s-sre-devops
Мой мини проект на СРЕ/ДевОпс позицию
Я решил манифесты для удобства, так что вот мой порядок их применения.

Сначала наш неймспейс
```bash
kubectl apply -f wa_ns.yaml
```
Затем деплой
```bash
kubectl apply -n webapp -f wa_deployment.yaml
```
Дальше сервис
```bash
kubectl apply -n webapp -f wa_svc.yaml
```
После это авто скейлер подов
```bash
kubectl apply -n webapp -f wa_horiz_auto_scale.yaml
```
Ну и под конец уменьшим шансы даунтайма
```bash
kubectl apply -n webapp -f wa_disrupt_budget.yaml
```
Надеюсь вам понравилось!
