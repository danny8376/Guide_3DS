# 문제 해결 (MSET9)

이 페이지는 "boot9strap 설치 (MSET9)", "boot9strap 설치 (MSET9 CLI)", 또는 "boot9strap 설치 (MSET9 Play 스토어)" 페이지에서 흔히 일어나는 문제에 관한 해결책을 기재합니다. 만약 이 페이지의 해결책만으로 문제를 해결할 수 없다면, [Nintendo Homebrew Discord 서버](https://discord.gg/MWxPgEp)에 들어가서 당신의 문제와 시도한 해결책을 설명해 주세요.

## MSET9 (application / script)

:::details Python 3 is not installed

Python이 사용중인 컴퓨터에 설치되지 않았습니다. [Python 웹사이트](https://www.python.org/downloads/) 에서 다운로드한 다음, 설치 프로그램을 더블 클릭한 다음, Python을 설치해 주세요. Python 설치가 완료된 뒤, 다시 시도해주세요.

:::

:::details ModuleNotFoundError: No module named 'pyfatfs'

The pyfatfs module, which is needed to use the MSET9 installer on macOS, isn't installed on your computer.

1. Open a separate Terminal window
2. Type `python3 -m pip install pyfatfs`, then press Enter
3. Start again from [Section I Step 3](installing-boot9strap-\(mset9-cli\)#section-i---prep-work)

:::

:::details HOME Menu extdata: Missing!

SD 카드를 삽입한 채로 콘솔의 전원을 켜고, MSET9의 상태를 다시 확인하세요.

만약 이래도 작동하지 않으면, SD 카드를 포맷해야 합니다:

1. SD 카드의 전체 데이터를 PC에 복사해두세요
2. SD 카드를 포맷해 주세요 ([Windows](formatting-sd-\(windows\)), [Linux](formatting-sd-\(linux\)), [macOS](formatting-sd-\(mac\)))
3. PC에 복사해둔 데이터를 다시 SD 카드에 복사해 주세요
4. [섹션 I 7단계](installing-boot9strap-\(mset9-cli\)#section-i---prep-work) 부터 다시 시작하세요.

:::

:::details Mii Maker extdata: Missing!

Mii Maker data was not found on the SD card. Please power on your console with your SD inserted, then launch Mii Maker, then check the MSET9 status again.

만약 이래도 작동하지 않으면, SD 카드를 포맷해야 합니다:

1. SD 카드의 전체 데이터를 PC에 복사해두세요
2. SD 카드를 포맷해 주세요 ([Windows](formatting-sd-\(windows\)), [Linux](formatting-sd-\(linux\)), [macOS](formatting-sd-\(mac\)))
3. PC에 복사해둔 데이터를 다시 SD 카드에 복사해 주세요
4. [섹션 I 8단계](installing-boot9strap-\(mset9-cli\)#section-i---prep-work) 부터 다시 시작하세요.

:::

:::details Title database: Not initialized!

Ensure that you have reset the title database.

- Please power on your console with your SD inserted
- 본체 설정을 실행한 후 `데이터 관리` -> `Nintendo 3DS 데이터 관리` -> `소프트웨어 관리` -> 초기화 ([영어 사진](/images/screenshots/database-reset.jpg))로 이동해 주세요.
    - 이 과정은 데이터를 삭제하지 않습니다.
- If you get a reset prompt, after resetting, power off your console and start again from [Section I Step 14](installing-boot9strap-\(mset9-cli\)#section-i---prep-work)

If you do _not_ getting a reset prompt, your SD card needs to be formatted:

1. SD 카드의 전체 데이터를 PC에 복사해두세요
2. SD 카드를 포맷해 주세요 ([Windows](formatting-sd-\(windows\)), [Linux](formatting-sd-\(linux\)), [macOS](formatting-sd-\(mac\)))
3. PC에 복사해둔 데이터를 다시 SD 카드에 복사해 주세요

<!--@include: ./_include/mset9-chorus.md -->

1. 콘솔의 모델과 버전을 입력한 다음 엔터키를 눌러주세요
2. Type `2` then press enter to check the MSET9 status
    - This will create the dummy databases again
3. Close the MSET9 script window
4. Start again from [Section I Step 12](installing-boot9strap-\(mset9-cli\)#section-i---prep-work).

:::

:::: details Error 01: Couldn't find Nintendo 3DS folder

You are not running MSET9 from the root of the SD card, or the SD card is missing the Nintendo 3DS folder.

Remember, your SD card should look like this:

::: info

![](/images/screenshots/mset9/mset9-root-layout.png)

:::

If your SD card layout is correct, then your SD card most likely isn't being read by your console and needs to be formatted:

1. SD 카드의 전체 데이터를 PC에 복사해두세요
2. SD 카드를 포맷해 주세요 ([Windows](formatting-sd-\(windows\)), [Linux](formatting-sd-\(linux\)), [macOS](formatting-sd-\(mac\)))
3. PC에 복사해둔 데이터를 다시 SD 카드에 복사해 주세요
4. Start again from the beginning of [Section I](installing-boot9strap-\(mset9-cli\)#section-i---prep-work)

::::

:::details Error 02: Your SD is write protected

Write-protection is enabled on this SD card. If you are using a full-size SD card, ensure that the lock is flipped in the [upright position](/images/sdlock.png). Otherwise, try ejecting and reinserting your SD card.

:::

:::details Error 04: You don't have 1 ID0, you have (#)!

You have multiple ID0 folders. To determine the correct folder, follow these instructions:

1. `Nintendo 3DS` 폴더를 `BACKUP_Nintendo 3DS` 폴더로 이름을 변경해 주세요
2. SD 카드를 콘솔에 다시 삽입해 주세요
3. 콘솔의 전원을 켜 주세요
4. 콘솔이 SD 카드 데이터를 생성할 때까지 기다려 주세요
    - Your applications will have disappeared. 이는 정상이며, 잠시 후에 고쳐질 것입니다.
5. 콘솔의 전원을 꺼 주세요
6. SD 카드를 컴퓨터에 삽입해 주세요
7. SD 카드의 `Nintendo 3DS` 폴더를 열어 주세요
8. Write down the first few characters of the folder you see
    - This is your true ID0, which we will keep in the real Nintendo 3DS folder
9. Delete the ID0 from the current `Nintendo 3DS` folder
10. Move the true ID0 folder from the `BACKUP_Nintendo 3DS` folder to the `Nintendo 3DS` folder
11. If it exists, move the `Private` folder from the `BACKUP_Nintendo 3DS` folder to the `Nintendo 3DS` folder

Once you've done this, continue from [Section I Step 3](installing-boot9strap-\(mset9-cli\)#section-i---prep-work).

:::

:::: details Error 05: You don't have 1 ID1, you have (#)!

<!--@include: ./_include/id1-check.md -->

::::

:::details Error 06: You need at least 16MB free

Your SD card does not have enough space to trigger MSET9. Free up some space and try again.

At the end of this guide, you will need at least 1.3GB to make a NAND backup, so it's best to free up at least that much.

:::

:::details Error 07: One or more files are missing or malformed!

One or more files that MSET9 needs to run is missing or corrupted. Re-download the [MSET9 Release `.zip`](https://github.com/hacks-guide/MSET9/releases/latest) and extract it to the root of your SD card, replacing all existing files, then try again.

:::

:::: details Error 18: Windows Locale Settings are broken!

<!--@include: ./_include/winerror234.md -->

::::

## MSET9 (exploit)

:::details Red screen after reinserting SD card (Section II Step 11)

You may be missing `SafeB9S.bin` from the root of your SD card, or the file may be corrupted. Copy it from the MSET9 `.zip`, replacing any existing files then follow these instructions to remove the trigger file:

1. Force power off your console by holding the Power button for 20 seconds
2. SD 카드를 컴퓨터에 삽입해 주세요

<!--@include: ./_include/mset9-chorus.md -->

1. 콘솔의 모델과 버전을 입력한 다음 엔터키를 눌러주세요
    - 현재 상태가 [Injected](/images/screenshots/mset9/mset9-injected.png)로 표시되어야 합니다
    - If you have already removed the trigger file (or never injected in the first place), the current state will show [Ready](/images/screenshots/mset9/mset9-ready.png), and you may [retry Section II](installing-boot9strap-\(mset9-cli\)#section-ii---mset9)
2. Type `4`, then press Enter
3. Once the window says "Removed trigger file", type `0` and then press Enter
4. Reinsert the SD card into your console
5. 콘솔의 전원을 켜 주세요
6. Return to [Section II Step 1](installing-boot9strap-\(mset9-cli\)#section-ii---mset9)

Alternatively, your SD card may be improperly formatted or partitioned. After removing the trigger file, format it:

1. SD 카드의 전체 데이터를 PC에 복사해두세요
2. SD 카드를 포맷해 주세요 ([Windows](formatting-sd-\(windows\)), [Linux](formatting-sd-\(linux\)), [macOS](formatting-sd-\(mac\)))
3. PC에 복사해둔 데이터를 다시 SD 카드에 복사해 주세요
4. Start again from from [Section II Step 1](installing-boot9strap-\(mset9-cli\)#section-ii---mset9)

:::

:::details System Settings loading infinitely after reinserting the SD card

You most likely did something different from the MSET9 instructions, selected the wrong model/version, or your SD card needs to be formatted. Ensure you are choosing the correct [model](/images/3dsmodels.png) and firmware version when opening the script.

Follow these instructions to remove the trigger file and to retry Section II:

1. Force power off your console by holding the Power button for 20 seconds
2. SD 카드를 컴퓨터에 삽입해 주세요

<!--@include: ./_include/mset9-chorus.md -->

1. 콘솔의 모델과 버전을 입력한 다음 엔터키를 눌러주세요
    - 현재 상태가 [Injected](/images/screenshots/mset9/mset9-injected.png)로 표시되어야 합니다
    - If you have already removed the trigger file (or never injected in the first place), the current state will show [Ready](/images/screenshots/mset9/mset9-ready.png), and you are ready to retry Section II
2. Type `4`, then press Enter
3. Once the window says "Removed trigger file", type `0` and then press Enter
4. Reinsert the SD card into your console
5. 콘솔의 전원을 켜 주세요
6. Return to [Section II Step 1](installing-boot9strap-\(mset9-cli\)#section-ii---mset9)

If you continue to have this issue and are sure that you did everything correctly, ensure the trigger file is removed and format your SD card:

1. SD 카드의 전체 데이터를 PC에 복사해두세요
2. SD 카드를 포맷해 주세요 ([Windows](formatting-sd-\(windows\)), [Linux](formatting-sd-\(linux\)), [macOS](formatting-sd-\(mac\)))
3. PC에 복사해둔 데이터를 다시 SD 카드에 복사해 주세요
4. Start again from from [Section II Step 1](installing-boot9strap-\(mset9-cli\)#section-ii---mset9)

:::

:::details An exception occurred after triggering MSET9

이미 커스텀 펌웨어가 설치되어 있을 수 있습니다. [CFW 확인](checking-for-cfw) 을 하는 것을 권장합니다.

:::

## SafeB9SInstaller와의 문제

<!--@include: ./_include/troubleshooting-sb9si-bin.md -->

<!--@include: ./_include/troubleshooting-sb9si-common.md -->

<!--@include: ./_include/troubleshooting-get-help-common.md -->

---

::: tip

[boot9strap 설치 (MSET9 CLI)](installing-boot9strap-\(mset9-cli\))로 돌아갑니다

:::

::: tip

[boot9strap 설치 (MSET9 Play 스토어)](installing-boot9strap-\(mset9-play-store\))로 돌아갑니다

:::

<!--@include: ./_include/troubleshooting-return.md -->


