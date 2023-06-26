# Android Sunflower с Compose

Приложение для садоводства, демонстрирующее лучшие практики разработки для Android при переносе приложения на Jetpack Compose.

**Чтобы узнать о том, как Sunflower был перенесен на Compose, смотрите документ [migration journey](docs/MigrationJourney.md) document.**

Этот пример демонстрирует:
* Использование Compose в существующем приложении: включая интеграцию со строками, ресурсами, темами и стилями.
* Интеграция с существующей архитектурой, основанной на библиотеках Jetpack.
* Реализация поведения `CollapsingToolbarLayout` вручную с помощью Compose.
* Показывает [Snackbars](https://material.io/components/snackbars) с помощью Compose..
* Использование Compose внутри `RecyclerView` ([#766](https://github.com/android/sunflower/pull/766))

## Функции

Экран [plant details screen](app/src/main/java/com/google/samples/apps/sunflower/PlantDetailFragment.kt) details screen Sunflower
строится с помощью Compose, а также элемент списка растений [plant list item](app/src/main/java/com/google/samples/apps/sunflower/compose/plantlist/PlantListItemView.kt)
внутри RecyclerView.

Весь код Compose можно найти в папке `compose`
[folder](app/src/main/java/com/google/samples/apps/sunflower/compose).

**Примечание**:  Так как Compose пока не может отображать HTML-код в `Text` . API `AndroidViewBinding` используется 
для вставки `TextView` в Compose. Смотрите композицию `PlantDescription` в файле
[PlantDetailView file](app/src/main/java/com/google/samples/apps/sunflower/compose/plantdetail/PlantDetailView.kt).