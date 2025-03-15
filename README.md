# yolo_necrotics
Некруха с моделью yolo

Ссылка на оригинал: https://github.com/ultralytics/ultralytics/blob/main/ultralytics/cfg/models/README.md

## Про параметры:
#### Scales:
* depth (глубина)-> коэффициент, определяющий количество слёв в модели. Чем больше, тем глубже;
* width (ширина)-> коэффициент, который регулирует количество каналов в свёрточных слоях (feature maps);
* max_channels (максимальное количество каналов)-> максимальное количество каналов в свёрточных сетях, которое может быть использовано на любом уровне;
#### Backbone:
* from -> индекс входного тензора, "-1" показывает, что вход берётся из предыдущего слоя;
* repeats -> количество раз, которое модулю повторяется (3 означает чтор модуль будет дублирован трижды);
* module -> название используемого слоя (Conv, C2f, SPPF):
    * Conv ->
    * C2f ->
    * SPPF ->
* args -> аргументы, передаваемые в модуль (количество каналов, размер ядра, шаг, и т д)
#### Head:
P1/2, P2/4 и т д обозначают уровни пиромиды признаков: FPN
* FPN (Feature Piramids Network) - представляет из себя экстрактор функций, который принимает в качестве данных одномасштабное изображение (произвольного размера), и выводит карты объектов полностью свёрточным способом