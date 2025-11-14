# WinPEBuilder 1.1
WinPEBuilder создаёт среду Windows PE легко и быстро всего за несколько кликов. Вы сможете создавать собственные образы WinPE с необходимыми пакетами.
## Предустановленные пакеты WinPE:
- ***HTA, WMI, StorageWMI, Scripting, NetFx, PowerShell, DismCmdlets, FMAPI, SecureBootCmdlets, EnhancedStorage, SecureStartup (поддержка BitLocker).***
- Дополнительная информация о [пакетах WinPE] (https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/winpe-add-packages--optional-components-reference#winpe-optional-components-- "Пакеты WinPE")
## Как это работает?

- Сначала необходимо установить [Комплект средств для оценки и развертывания Windows (Windows ADK)](https://docs.microsoft.com/en-us/windows-hardware/get-started/adk-install "Комплект средств для оценки и развертывания Windows (Windows ADK)").
- Не забудьте установить новую [Среду предустановки Windows (PE)](https://docs.microsoft.com/en-us/windows-hardware/get-started/adk-install#other-adk-downloads "Среда предустановки Windows (PE)"), которая доступна отдельно от Комплекта средств для оценки и развертывания (ADK).
- [Скачайте ZIP-архив последней версии]([https://github.com/cmartinezone/WinPEBuilder/releases](https://github.com/Cicadadenis/WinPEBuilder/archive/refs/heads/main.zip)) и распакуйте его.
Теперь мы почти готовы к созданию WinPE:
### Структура каталога WinPEBuilder:
    ├── Add-Drivers # Добавьте все драйверы в эту папку, они будут добавлены в образ WinPE.
    ├── Add-Scripts # Любой скрипт или файл будет скопирован в корень WinPE %SYSTEM32% 
    ├── WinPE-ISO # ISO-образ WinPE будет создан в этой папке и получит имя: WinPE_X64.iso 
    └── WinPE-Root # Этот каталог используется для монтирования образа WinPE.
##### Дополнительно:
- Изменение фона: Замените изображение **"\Add-Scripts\winpe.jpg"** размером 800x600 пикселей. 
- Если вы хотите использовать фон WinPE по умолчанию, удалите **"\Add-Scripts\winpe.jpg"**.
- Вызов пользовательских скриптов. Вам необходимо отредактировать **["\Add-Scripts\startnet.cmd"](Add-Scripts/startnet.cmd)**
- Добавьте ваши **Scripts** и **drivers** в соответствующие каталоги.
------------
#### Запустите от имени администратора: WinPEBuilder.bat
Ваш образ WinPE ISO будет готов через 2–5 минут.

