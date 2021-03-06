# Домашнее задание к лекции ШРИ - мультимедиа

В этом задании мы будем делать страницу видеонаблюдения в умном доме.

На странице можно смотреть HLS видеопотоки с веб-камер, переключать камеры,
накладывать риал-таймовые фильтры на видео и следить за активностью в умном доме.

Для разработки вы можете использовать тестовые видео-потоки
(о том, как их развернуть, можно почитать [тут](#TODO).

Страница "Видеонаблюдение" должна работать в актуальной версии Chrome на десктопе и
на Android/iOS (достаточно одной платформы – укажите в описании ДЗ, на какой ОС вы отлаживались).

Для проигрывания HLS-потока на платформах без нативной поддержки HLS воспользуйтесь библиотекой [hls.js](https://github.com/video-dev/hls.js/).

## Пункты, которые нужно реализовать

1. **Страница-вкладка в интерфейсе умного дома "Видеонаблюдение"**:

    На странице должна находиться сетка из 4-ёх видео-превью.
    Клик по превью разворачивает соответствующее видео на всю страницу.
    
    Анимацию разворачивания видео можно сделать по аналогии с маковским приложением 
    Photo Booth (или посмотреть видео по (ссылке)[https://yadi.sk/i/shdHcVlkd_BO1w]).
    
    Когд видео раскрыто на всю страницу, в интерфейсе нужно предусмотреть кнопку
    "Все камеры", которая позволяет вернуться назад.
    
    Анимация переключения видео должна работать без тормозов (без просадки FPS на странице)
    
2. **Фильтры для видео**:

    Видео-поток с камеры может быть плохого качества (размытый, засвеченный или затемненный) - добавьте на экран просмотра видео
    возможность регулировать его яркость и контрастность.
    
    Для контролов настройки яркости/контрастности можете реиспользовать слайдеры из вашего
    вступительного задания, либо просто используйте `input` (реализация контрола не будет оцениваться дополнительно).
    
3. **Анализатор звука**:

    Реализуйте анализатор громкости звука в потоке из открытой камеры (в виде столбчатой диаграммы).

## Бонусные задания

1. Добавьте информацию об уровне освещенности в комнате, в которой стоит камера.
2. Реализуйте детектор движения в видео-потоке (нарисуйте поверх видео прямоугольник, ограничивающий область, в которой происходит движение).

Работа анализаторов не должна давать серьезных просадок FPS.

## Формат сдачи

Укажите в тикете ссылку на репозиторий, отчет по выполненным пунктам задания и способу их реализации, и инструкцию для запуска.
