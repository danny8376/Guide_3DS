# ntrboot

::: danger

NDS Card has [suspended outgoing packages to the United States](https://nds-card.com/NewsShow.asp?NewsID=1344). All product links listed below may not ship to the United States. For further support (in English), join [Nintendo Homebrew on Discord](https://discord.gg/MWxPgEp).

:::

::: tip

フラッシュカードが ntrboot で事前にフラッシュされた場合 (または ntrboot をフラッシュ済み) [boot9strapのインストール (ntrboot)](installing-boot9strap-\(ntrboot\)) をスキップして使用方法を説明します。

:::

## Required Reading

Ntrbootを使ってboot9strapをインストールするには互換性のあるNDSフラッシュカードが必要です。 これらのフラッシュカートのいくつかはntrbootを事前にフラッシュして販売されていることに注意してください。

While the ntrboot exploit works independently of the system version, the ntrboot flasher (which installs the exploit to the cart) is not. This means that, depending on the versions and consoles supported by your flashcart, only certain methods may be available to you.

「Time Bomb」があるカートは、起動できなくなる日付があることに注意してください。 システムクロックがフラッシュカードのファームウェアによって決定された日付に達したことを検出すると、.nds\`ファイルが起動できなくなります。 これを避ける1つの方法は、システムクロックを以前の日付に設定することです。

| Flashcart Name                                                                                                              |          Current Price |                       "Time Bomb"?                       |                                 3DS Versions?                                 |                           DSi Versions?                           | Other Notes                                                                                                                                                                                                                                                                                                |
| --------------------------------------------------------------------------------------------------------------------------- | ---------------------: | :------------------------------------------------------: | :---------------------------------------------------------------------------: | :---------------------------------------------------------------: | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**Ace3DS X**](https://www.nds-card.com/ProShow.asp?ProID=575)                                                              | $17.99 |                            No                            |                                      ALL                                      |                                ALL                                | **Comes pre-flashed with ntrboot** (external switch to switch between ntrboot ("3DS") and NDS modes); do not manually flash with ntrboot. This cart needs an SD card inserted to function for both ntrboot and regular NDS firmware. |
| [**R4i-SDHC B9S** (r4i-sdhc.com)](http://www.nds-card.com/ProShow.asp?ProID=574)         | $16.99 |                     September 3, 2024                    |                                      ALL                                      |                                ALL                                | **Comes pre-flashed with ntrboot**; can be flashed back to an NDS flashcart.                                                                                                                                                                                                               |
| [**DSTT** (ndstt.com)](http://www.nds-card.com/ProShow.asp?ProID=157)                    | $11.99 |                            No                            |                                      None                                     |                                None                               | Only models with [certain flash chips](https://gist.github.com/aspargas2/fa2a70aed3a7fe33f1f10bc264d9fab6) are compatible with ntrboot.                                                                                                                                                    |
| [**R4i-SDHC 3DS RTS** (r4i-sdhc.com)](http://www.nds-card.com/ProShow.asp?ProID=146)     | $15.99 | 1.85b: September 3, 2024 |                                      ALL                                      |                                ALL                                |                                                                                                                                                                                                                                                                                                            |
| [**R4iSDHC GOLD Pro 20XX** (r4isdhc.com)](http://www.nds-card.com/ProShow.asp?ProID=490) | $17.99 |  4.0b: September 3, 2024 |                                      ALL                                      |                                ALL                                | Only r4isdhc **.com** carts marked with a year of 2014 or later are compatible.                                                                                                                                                                                            |
| **Ace3DS Plus**                                                                                                             |                        |                            No                            |                                      ALL                                      |                                ALL                                | This cart needs an SD card inserted to function for both ntrboot and regular NDS firmware.                                                                                                                                                                                                 |
| **Acekard 2i**                                                                                                              |                        |                            No                            |       <= 4.3.0       | <= 1.4.4 |                                                                                                                                                                                                                                                                                                            |
| **Gateway Blue**                                                                                                            |                        |                            No                            | 4.1.0 - 4.5.0 |                                ALL                                |                                                                                                                                                                                                                                                                                                            |
| **Infinity 3 R4i** (r4infinity.com)                                                      |                        |                            No                            |                                      ALL                                      |                                ALL                                |                                                                                                                                                                                                                                                                                                            |
| **R4 3D Revolution**                                                                                                        |                        |                            No                            |                                      None                                     |                                None                               |                                                                                                                                                                                                                                                                                                            |
| **R4i Gold 3DS Plus** (r4ids.cn)                                                         |                        |                            No                            |                                      ALL                                      |                                ALL                                | **Comes pre-flashed with ntrboot** ([internal switch to switch between ntrboot and NDS modes](/images/screenshots/r4i-gold-3ds-plus.png)); do not manually flash with ntrboot.                                                                                          |
| **R4i Gold 3DS** (r4ids.cn)                                                              |                        |                            No                            |                                      ALL                                      |                                ALL                                | All carts are compatible.                                                                                                                                                                                                                                                                  |
| **R4i Ultra** (r4ultra.com)                                                              |                        |                            No                            |       <= 4.3.0       |                                ALL                                |                                                                                                                                                                                                                                                                                                            |
| **R4i-SDHC 3DS RTS Deluxe Edition**                                                                                         |                        |                          Unknown                         |                                      ALL                                      |                                ALL                                | Only the Deluxe Edition with the blue sticker is compatible.                                                                                                                                                                                                                               |
| **R4iSDHC RTS LITE 20XX** (r4isdhc.com)                                                  |                        |  4.0b: September 3, 2024 |                                      ALL                                      |                                ALL                                | Only r4isdhc **.com** carts marked with a year of 2014 or later are compatible.                                                                                                                                                                                            |
| **R4iSDHC Dual-Core 20XX** (r4isdhc.com)                                                 |                        |  4.0b: September 3, 2024 |                                      ALL                                      |                                ALL                                | Only r4isdhc **.com** carts marked with a year of 2014 or later are compatible.                                                                                                                                                                                            |

::: info

![](/images/screenshots/ntrboot-flashcarts.png)

:::

Ensure your flashcart is able to launch `.nds` files on your console before beginning. フラッシュカードによっては、ファームウェアまたはカーネルファイルをフラッシュカードのSDカードにコピーする必要がある場合があります。 詳細については、特定のフラッシュカートの手順を参照してください。

特定のメソッドは追加の互換性情報を持つ可能性があることに注意してください。

The usage of this exploit, regardless of the flashing method, requires access to a small magnet if the target console is of a folding style (any 3DS family system that is not the old 2DS with a sleep switch). This is because the exploit requires your console to enter sleep mode while still having access to the buttons.

::: info

To test if a magnet will work, hold it on or around the (A)(B)(X)(Y) buttons while the console is powered on to see if it triggers sleep mode. その場合、磁石がその場所にある限り、両方のディスプレイは黒くなります。

:::

ntrbootエクスプロイトがインストールされている間は、フラッシュカードは標準機能では使用できないことに注意してください(Acekard 2iの場合を除く)。 NDSとカスタムファームウェア3DSシステムのみ\*で機能し続けます。 This means that, for most flashcarts, it will not even display on the HOME Menu. 完了したら、ntrbootのインストール手順の最後にオプションの手順を実行して、フラッシュカードから削除する手順があります。

::: danger

稀ですが、フェイクのフラッシュカードを**文鎮化**する可能性があります。 This is unlikely, but nevertheless, only original listed flashcarts are supported. To reduce the chance of receiving a counterfeit card, it is recommended that you use a reputable site to buy your flashcart (such as [NDS Card](https://www.nds-card.com/)).

:::

___

## Methods

___

### Flashing ntrboot (3DS Single System)

この方法は、改造されていない3DSと対応しているフラッシュカード以外の必要の物は必要ありません。 この方法は、フラッシュカードを使い、ntrbootフラッシャーが入っている`.nds`ファイルを実行します。 このことは、`.nds`を3DSで実行するのにフラッシュカードが対応していることが必要です。 詳細については、上記のflashcartの表を参照してください。

::: tip

[ntrbootのフラッシュ (3DSシングルシステム)](flashing-ntrboot-\(3ds-single-system\)) へ進んでください

:::

___

### Flashing ntrboot (3DS Multi System)

This method requires temporary access to a second 3DS family console that is already running boot9strap. フラッシュカードが3DSのいずれかのバージョンをサポートする必要はありません。

::: tip

[ntrbootのフラッシュ (3DSマルチシステム)](flashing-ntrboot-\(3ds-multi-system\)) へ進んでください

:::

___

### Flashing ntrboot (NDS)

この方法では、フラッシュカードと互換性のあるNintendoDSもしくはNintendoDS Liteにアクセスする必要があります。 この方法は、フラッシュカードを使い、ntrbootフラッシャーが入っている`.nds`ファイルをNDSにて実行します。

::: tip

[ntrbootのフラッシュ (NDS)](flashing-ntrboot-\(nds\)) へ進んでください

:::

___

### Flashing ntrboot (DSi)

この方法では、フラッシュカードと互換性のあるNintendoDSiにアクセスする必要があります。 この方法は、フラッシュカードを使い、ntrbootフラッシャーが入っている`.nds`ファイルをDSiにて実行します。 このことは、`.nds`をDSiで実行するのにフラッシュカードが対応していることが必要です。 詳細については、上記のflashcartの表を参照してください。

::: tip

[ntrbootのフラッシュ (DSi)](flashing-ntrboot-\(dsi\)) へ進んでください

:::
