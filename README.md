# 🌊 Waveshare ESP32-P4 86 Panel (Custom Fork)

> ⚠️ **注意**：本分支是基于原版固件的修改版本，专为中文用户及特定需求优化。
> **构建环境**：ESPHome 2025.11.5

## 🛠️ 本仓库修改说明 (Custom Modifications)

在原作者优秀工作的基础上，本仓库进行了以下增强与修复：

### ✨ 新增功能 (Features)
1.  **🇨🇳 全面汉化与中文支持**
    * 系统界面已预设为简体中文。
    * **修复字体渲染**：解决了媒体播放器（Media Player）界面中，中文歌曲名和艺术家名称显示为方块（乱码）的问题，现在可以完美显示中文曲目信息。
2.  **🔊 语音助手交互增强**
    * 新增了**唤醒提示音**功能。当通过语音唤醒设备（卫星模式）时，设备会播放一段提示音，提供明确的听觉反馈。

### 🐛 已知问题 (Known Issues)
*基于 ESPHome 2025.11.5 版本测试*

1.  **符号显示限制**：中文标点或生僻符号暂时无法显示（缺字），计划在后续修复。
2.  **UI 数据异常**：主页天气卡片中的“风速”数值显示可能存在异常，暂未修复。
3.  **🚫 语言切换警告**：
    * 固件默认已锁定为**简体中文**。
    * **请勿点击设置中的“语言切换”（旗帜图标）**。由于底层图片资源索引问题，点击切换语言会导致设备立即崩溃并重启（Boot Loop）。

---

## 🙏 致谢 (Credits)

特别感谢原作者 **[@alaltitov](https://github.com/alaltitov)** 开源了这个精彩的项目！本仓库的所有工作均基于其杰出的代码库构建。如果你喜欢这个项目，请务必去原仓库点一颗 ⭐️ Star。

---

## 👇 以下为原仓库 README 内容 (Original README)
# LVGL ESPhome Waveshare-ESP32-P4-86-Panel-ETH-2RO custom firmware

<p align="center">
 <img width="200px" src="/docs/images/loading.png">
 <img width="200px" src="/docs/images/home.png">
 <img width="200px" src="/docs/images/forecasts.png">
 <img width="200px" src="/docs/images/info.png">
 <img width="200px" src="/docs/images/settings.png">
 <img width="200px" src="/docs/images/light0.png">
 <img width="200px" src="/docs/images/light1.png">
 <img width="200px" src="/docs/images/climate0.png">
 <img width="200px" src="/docs/images/climate1.png">
 <img width="200px" src="/docs/images/climate2.png">
 <img width="200px" src="/docs/images/climate3.png">
 <img width="200px" src="/docs/images/media_player.png">
 <img width="200px" src="/docs/images/vacuum.png">
</p>

<p align="center">
    <img alt="Static Badge" src="https://img.shields.io/badge/made%20by-alaltitov-blue">
    <img alt="Static Badge" src="https://img.shields.io/badge/version-v1.0%20Dev-green">
    <img alt="Static Badge" src="https://img.shields.io/badge/esphome min version-2025.11.0-red">
    <img alt="Static Badge" src="https://img.shields.io/badge/license-MIT-orange">
</p>

## Support the Project

<img src="/docs/images/donate.png" alt="QR Code" width="150" align="left" hspace="10"/>

<div style="padding-top: 40px;">
  <b>Support me on</b>
  <div style="height: 30px;"></div>
  <a href="https://boosty.to/altitov/donate">
    <img src="/docs/images/boosty.png" alt="Boosty" width="160"/>
  </a>
</div>

<br clear="all"/>

## Questions, Discussions, Ideas

<div style="padding-top: 40px;">
  <a href="https://t.me/esphome_lvgl_chats">
    <img src="/docs/images/t_me_chats.jpg" alt="QR Code" width="150" align="left" hspace="10"/>
  </a>
</div>

<br clear="all"/>

## ⚠️ Important Notice
- You'll need the DEV version of ESPHome 2025.11.0.

## ✨ Features

- Status indicators for Wi-Fi, Home Assistant API, thermostat, air conditioner, touchscreen lock, alarm panel
- Weather icons with current conditions and temperature
- Weather Forecasts daily and hourly
- Date and time
- Sensor readings from Home Assistant
- Voice Assistant (testing...)
- Lights control
- Alarm Panels control
- Climate control
- Covers control
- Fans control
- Media Player control
- Radio control (testing...)
- Vacuum control
- Settings:
  * Backlight adjustment
  * Screen timeout settings
  * Language selection:
    - ru (from [alaltitov](https://github.com/alaltitov))
    - en (from [alaltitov](https://github.com/alaltitov))
    - pl (from [reaper7](https://github.com/reaper7))
    - fr (from [lboue](https://github.com/lboue))
    - es (from Antonio)
    - nl (from [zjean](https://github.com/zjean))
    - si (from [Protoncek](https://github.com/Protoncek))
    - it (from [echopage1964](https://github.com/echopage1964))
    - de (from [MATZE-MAN](https://github.com/MATZE-MAN))

## 📦 Installation
> 📹 **Video [instruction](https://youtu.be/HYN_2hvcbes?si=JfYQH4vCuFlr8Q9r)**

<img width="400px" src="/docs/images/ha_options.png">

- You must enable the "Allow the device to perform Home Assistant actions." option in the ESPHome integration to Home Assistant to control devices.
- Install custom component for forecasts and covers for media player from [here](https://github.com/alaltitov/homeassistant-display-tools).
- Copy repository to vscode or to esphome folder of your Home Assistant. Change substitutions.yaml and config.yaml your entities in all widgets (only in substitution, in code everything will be substituted automatically).

## 📖 Documentation
- [ESPHome LVGL 8.4](https://esphome.io/components/lvgl/)

## 🤝 Thanks for your help
- Thanks to [ZHNovell](https://github.com/ZHNovell) for financial support of the project, as well as for help with testing and ideas.
- Thanks, [сlydebarrow](https://github.com/clydebarrow), [jesserockz](https://github.com/jesserockz), [ssieb](https://github.com/ssieb) for helping me with the project!

