# Справочник API

## Основные классы

<u>Ключевые классы приложения:</u>

- **MainActivity** - главная активность
- **DrawView** - кастомное view для рисования
- **SecondActivity** - обработка касаний

## Методы DrawView

```java
public class DrawView extends View {
    // Обновление масштабированных точек
    private void updateScaledPoints() {
        for (int i = 0; i < points.length; i += 2) {
            float dx = originalPoints[i] - centerX;
            float dy = originalPoints[i + 1] - centerY;
            currentPoints[i] = centerX + dx * scaleFactor;
            currentPoints[i + 1] = centerY + dy * scaleFactor;
        }
    }
    
    @Override
    protected void onDraw(Canvas canvas) {
        // Отрисовка графики
    }
}
```

## Константы и настройки

<u>Важные константы:</u>

```java
private static final float MIN_ZOOM = 0.5f;    // Минимальный зум
private static final float MAX_ZOOM = 3.0f;    // Максимальный зум
private static final int MAX_TOUCHES = 10;     // Макс. касаний
```

## События и колбэки

[ Подробнее о жестах](../features/gestures.md) | [ Графические методы](../features/graphics.md)

[ К содержанию](../README.md)