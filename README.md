e480-monterey
Hackintosh macOS Big Sur and Monterey ThinkPad E480
`OpenCore 0.7.5`

Проверено на:

- 11.~ Big Sur
- 12.~ Monterey

## Disclaimer

Я не несу ответственности за любую потерю данных и повреждение оборудования. Все файлы и конфигурации представлены здесь исключительно в ознакомительных целях.

## Спецификации устройства

| Specifications | Details |
|:---|:---|
| Computer Model | ThinkPad E480 (2018) |
| CPU | Intel Core i5-8250U |
| Memory | DDR4 2400 Mhz. Установлено 2x8 GB |
| NVMe SSD | 256 GB Windows OS |
| SATA SSD | 240 GB Kingston A400 |
| Integrated Graphics | Intel UHD Graphics 620 |
| Ethernet | RTL8168/8111/8112 Gigabit Ethernet Controller |
| Sound Card | Conexant CX20753/4 (layout-id: 15) |
| Wireless Card | Замена на BCM94352Z (DM1560) |

## Что работает:

#### CPU

XCPM power management полностью поддерживается. HWP полностью доступен.

#### Battery

Уровень заряда отображается корректно.

#### Wi-Fi

Родной модуль BT/Wifi `Realtek 8821CE Wireless LAN 802.11ac PCI-E NIC` заменен на BCM94352Z (DM1560), который работает корректно.

#### USB

USB порты пропатчены через HackinTool, `5 Gbps` для USB 3.0.

#### Ethernet

Работает корректно.

#### Display

Встроенная графика `Intel UHD Graphics 620` с подменой ID работает коректно. объем видеопамяти установлен на 3072 MB.

HDMI работает корректно, в том числе и в режимах `2K@60Hz` и `4K@30Hz`.

#### Audio

Полностью работает через AppleALC с установленным значением `layout-id: 15`.

#### Keyboard

Работает корректно, за исключением кнопки Insert, Которой нет на клавиатуре MagicKeyboard.

#### SSD

NVMe и SATA накопители работают корректно, на всех накопителях TRIM включен по умолчанию.

#### Bluetooth, Handoff, Airplay, Airdrop

Работает корректно, Airdrop работает только между iPhone, iPad и Mac. 

#### Trackpad & Trackpoint

Работает корректно.

## Что не работает

Кнопка Fn перестает работать после сна. Это известный баг на ThinkPad E470, E480 E490, E570, E580, E590, etc.

## Рекомендованные настройки BIOS

> Убедитесь, что пароль Windows отключен перед входом в BIOS, вы больше не сможете входить в Windows с использованием PIN после выполнения конфигурации BIOS.

- Security
  - Intel SGX: Disabled
- Boot
  - Boot Mode: Both UEFI and Legacy
  - Boot Priority: UEFI First
  - Quick Boot: Enabled

### Гибернация

Работает корректно.

### Известные проблемы

- После выхода из режима сна имеется проблема с отображением заряда батареи (зависает на некоторое время). Как временное решение - еще раз отправить ноутбук в сон вручную. После пробуждения уровень заряда сразу будет отображаться корректно.
- Bluetooth гарнитуры (Ex. Airpods) иногда отключаются/переподключаются на расстоянии больше 2 метров.
- Airdrop работает только с iPhone на MacOS. 
Возможно, проблемы удасться решить.


## Благодарность

**(Original) ThinkPad E480 Hackintosh** [Sukka](https://github.com/SukkaW).
