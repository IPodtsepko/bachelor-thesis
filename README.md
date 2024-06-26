# Бакалаврская выпускная квалификационная работа

> [!NOTE]
> To read this document in English, follow the [link](README_EN.md).


Данный репозиторий содержит материалы моей дипломной работы на тему "Транскодирование JPEG-изображений при помощи предсказания коэффициентов ДКП на основе нейронной сети", которая была подготовлена мной при выпуске из бакалавриата кафедры компьютерных технологий Университета ИТМО. Защита проходила 7 июня 2024 г. Ниже представлена основная информация о работе.

### Содержание
- [АННОТАЦИЯ ВЫПУСКНОЙ КВАЛИФИКАЦИОННОЙ РАБОТЫ](#аннотация-выпускной-квалификационной-работы)
- [ХАРАКТЕРИСТИКА ВЫПУСКНОЙ КВАЛИФИКАЦИОННОЙ РАБОТЫ](#характеристика-выпускной-квалификационной-работы)
    - [Техническое задание](#техническое-задание)
    - [Цель исследования](#цель-исследования)
    - [Задачи, решаемые в ВКР](#задачи-решаемые-в-вкр)
    - [Краткая характеристика полученных результатов](#краткая-характеристика-полученных-результатов)
- [Структура репозитория](#структура-репозитория)


## АННОТАЦИЯ ВЫПУСКНОЙ КВАЛИФИКАЦИОННОЙ РАБОТЫ

**Обучающийся** Подцепко Игорь Сергеевич

**Факультет/институт/кластер** факультет информационных технологий и программирования

**Группа** M34381

**Направление подготовки** 01.03.02 Прикладная математика и информатика

**Образовательная программа** Информатика и программирование 2020

**Язык реализации ОП** Русский

**Квалификация** Бакалавр

**Тема ВКР** Транскодирование JPEG-изображений при помощи предсказания коэффициентов ДКП на основе нейронной сети

**Руководитель ВКР** Беляев Евгений Александрович, PhD, науки, Университет ИТМО, факультет информационных технологий и программирования, доцент (квалификационная категория "ординарный доцент")

## ХАРАКТЕРИСТИКА ВЫПУСКНОЙ КВАЛИФИКАЦИОННОЙ РАБОТЫ

#### Техническое задание

Разработать и обучить нейронную сеть, которая предсказывает часть коэффициентов дискретного косинусного преобразования (ДКП) из входного JPEG-изображения, и использовать полученные коэффициенты для энтропийного кодирования исходных коэффициентов.

#### Цель исследования

Изучить возможность и потенциал нейронных сетей для реализации этапа внутреннего предсказания коэффициентов ДКП при транскодировании JPEG-изображений.

#### Задачи, решаемые в ВКР

1. Реализовать декодирование JPEG-изображений с удалением (обнулением) части коэффициентов ДКП для подготовки набора данных для обучения нейронной сети;
2. Разработать и обучить нейронную сеть, которая предсказывает (вычисляет) часть коэффициентов ДКП на основании остальных коэффициентов;
3. Реализовать кодирование с предсказанием для сжатия выбранной части коэффициентов ДКП;
4. Оценить степень сжатия, которую удается достичь благодаря нейросетевому внутреннему предсказанию.

#### Краткая характеристика полученных результатов

Разработан метод внутреннего предсказания коэффициентов ДКП для транскодирования JPEG-изображений, основанный на применении нейронной сети и позволяющий сократить размер JPEG-файлов из подмножества набора данных ImageNet в среднем на 3,33% при медиане 3,38%. Наилучшее достигнутое сжатие составило 6,28%. Метод успешно комбинируется с утилитой Jpegtran, позволяющей заменять код Хаффмана на арифметическое кодирование, и общая степень сжатия в среднем составляет 13,16%.

## Структура репозитория

- [output](output) — PDF-файлы пояснительной записки и презентации, представленными к защите;
- [presentation](presentation) — исходники презентации в Figma;
- [program](program) — разработанная библиотека для транскодирования JPEG-изображений;
- [thesis](thesis) — исходники пояснительной записки в LaTeX.
