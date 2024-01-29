# Настройка на средата за програмиране в Minecraft Java Edition с Python

## Стъпка 1: Инсталиране на Minecraft Java Edition
Уверете се, че Minecraft Java Edition е инсталиран на вашия компютър.

## Стъпка 2: Инсталиране на Minecraft Server
1. Изтеглете последната версия на Minecraft Server от [официалния уебсайт на Minecraft](https://www.minecraft.net/en-us/download/server).
2. Създайте нова папка за Minecraft сървърните файлове и поставете изтегления `.jar` файл там.
3. Стартирайте сървъра за първи път, за да генерирате конфигурационни файлове, след което го затворете.
4. Отворете `eula.txt` и променете `eula=false` на `eula=true`, за да приемете условията на лиценза.

## Стъпка 3: Инсталиране на RaspberryJuice
1. Изтеглете последната версия на RaspberryJuice от [GitHub страницата на мода](https://github.com/zhuowei/RaspberryJuice).
2. Поставете изтегления `.jar` файл в папката `plugins` на вашата Minecraft сървърна директория. Ако папка `plugins` не съществува, създайте я.

## Стъпка 4: Стартиране на Minecraft сървъра
Стартирайте Minecraft сървъра отново, за да се зареди RaspberryJuice модът.

## Стъпка 5: Настройка на Python
1. Уверете се, че Python е инсталиран на вашата система.
2. Инсталирайте библиотеката `mcpi` или друга съвместима библиотека, използвайки pip: `pip install mcpi`.

## Стъпка 6: Тестване на връзката
Напишете прост Python скрипт, който се свързва с Minecraft сървъра и извършва основна задача, като например поставяне на блок.

### Примерен Python скрипт за тестване

```python
from mcpi.minecraft import Minecraft

# Свързване с Minecraft сървъра
mc = Minecraft.create("localhost", 4711)  # Заменете с порта, на който работи RaspberryJuice

# Поставяне на блок
x, y, z = mc.player.getPos()  # Вземане на позицията на играча
mc.setBlock(x+1, y, z, 1)  # Поставяне на каменен блок близо до играча
