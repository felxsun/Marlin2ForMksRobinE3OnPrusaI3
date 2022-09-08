# Marlin 2  - for Prusa i3 MK3 w. MKS Robin E3
### Based on Marlin 2.0 LST
[Marlin 2.0.9.5](https://github.com/MarlinFirmware/Marlin/tree/2.0.9.5)
<br>
<br>


## **Edit Note**  

  + 參考 ： [MKS Robin E3D V1.1主板使用说明书](https://blog.csdn.net/gjy_skyblue/article/details/119418639?spm=1001.2014.3001.5501)
---
## Platformio.ini
<details><summary>
    16 : 
    預設環境 mks_robin_e3
    </summary>
    <pre>
        default_envs = mks_robin_e3
    </pre>
</details>

---
## Configuration.h
<details><summary>63 : 組態作者</summary>
    誰改了這個檔案
</details>
<details><summary>64 : 使用客制化版本檔案</summary>
    <pre>#define CUSTOM_VERSION_FILE Version.h</pre>
</details>
<details><summary>90 : 主板型號 BOARD_MKS_ROBIN_E3D_V1_1</summary>
    <pre>#define MOTHERBOARD BOARD_MKS_ROBIN_E3D_V1_1</pre>
</details>
<details><summary>101 : 序列埠 1</summary>
    <pre>#define SERIAL_PORT 1</pre>
</details>
<details><summary>137 : 客制化機器名稱 "Felix Robin Prusa"</summary>
    <pre>#define CUSTOM_MACHINE_NAME "Felix Robin Prusa"</pre>
</details>
<details><summary>159~ : 驅動器型號 TMC2209</summary>
    <pre>
    #define X_DRIVER_TYPE  TMC2209
    #define Y_DRIVER_TYPE  TMC2209
    #define Z_DRIVER_TYPE  TMC2209
    #define E0_DRIVER_TYPE TMC2209
    </pre>
</details>
<details><summary>511~ : 溫度感測器  1: EPCOS thermistors</summary>
    <pre>
    #define TEMP_SENSOR_0 1
    #define TEMP_SENSOR_BED 1
    </pre>
</details>
<details><summary>779~ : 擠出保護  </summary>
    <pre>
    //#define PREVENT_COLD_EXTRUSION
    #define EXTRUDE_MINTEMP 170

    #define PREVENT_LENGTHY_EXTRUDE
    #define EXTRUDE_MAXLENGTH 200
    </pre>
</details>
<details><summary>1087 : Steps/mm (200,200,800,283)</summary>
    <pre>#define DEFAULT_AXIS_STEPS_PER_UNIT   { 200, 200, 800, 283 }</pre>
</details>
<details>
    <summary>
    <font color="red"><strong>1094</strong></font> : 
    最大速度 { 600, 600, 30, <font color="red"><strong>40</strong></font> }
    </summary>
    <pre>
        #原始值
        #define DEFAULT_MAX_FEEDRATE          { 600, 600, 30, 80 }
    </pre>   
</details>
<details><summary> 
    <font color="red"><strong>1107</strong></font> : 
    最大加速度 { 3000, 3000, 100, <font color="red"><strong>1000</strong></font> }
    </summary>
    <pre>#define DEFAULT_MAX_ACCELERATION      { 3000, 3000, 100, 10000 }</pre>
</details>
<details><summary>1190~ : Z歸位使用probe</summary>
    <pre>
    //#define Z_MIN_PROBE_USES_Z_MIN_ENDSTOP_PIN
    #define USE_PROBE_FOR_Z_HOMING
    </pre>
</details>   
<details><summary>1210 : Z軸Probe腳位  PB1</summary>
    <pre>#define Z_MIN_PROBE_PIN PB1</pre>
</details>
<details><summary>1230 : Probe型式 FIX_MOUNTED_PROBE</summary>
    <pre>#define FIX_MOUNTED_PROBE</pre>
</details>
<details><summary>1529~ : 各軸方向定義</summary>
    <pre>
    #define INVERT_X_DIR true
    #define INVERT_Y_DIR true
    #define INVERT_Z_DIR false
    </pre>
</details>
<details><summary>1577~ : 成型床尺吋</summary>
    <pre>
    #define X_BED_SIZE 230
    #define Y_BED_SIZE 210
    </pre>
</details>
<details>
    <summary>
        <strong><font color="red">1581~</font></strong> : 
        歸位後行程範圍 相對於限位器位置
    </summary>
    <pre>
    #define X_MIN_POS -10
    #define Y_MIN_POS -5
    #define Z_MIN_POS 0
    #define X_MAX_POS X_BED_SIZE
    #define Y_MAX_POS Y_BED_SIZE
    #define Z_MAX_POS 205
    </pre>
</details>
<details>
    <summary>
        <font color=red><strong>1642</strong></font>
         : 線料用盡檢測   N/A
    </summary>
    <pre>#define FILAMENT_RUNOUT_SENSOR</pre>
</details>
<details><summary>1742~ : 自動熱床平台校準 AUTO_BED_LEVELING_BILINEAR </summary>
    <pre>
    //#define AUTO_BED_LEVELING_3POINT
    //#define AUTO_BED_LEVELING_LINEAR
    #define AUTO_BED_LEVELING_BILINEAR
    //#define AUTO_BED_LEVELING_UBL
    //#define MESH_BED_LEVELING
    </pre>
</details>
<details><summary>1945 : Z 安全歸位, 避免Z在熱床之外歸位</summary>
    <pre>#define Z_SAFE_HOMING</pre>
</details>
<details><summary>1953 : 歸位速度 : 3000, 3000, 2400</summary>
    <pre>#define HOMING_FEEDRATE_MM_M { (50*60), (50*60), (40*60) }</pre>
</details>
<details><summary>2030 : 使用EEPROM存設定值</summary>
    <pre>#define EEPROM_SETTINGS</pre>
</details>
<details>
    <summary>
        <strong><font color="red">2036</font></strong> : 
        更新後自動初始化EEPROM</summary>
    <pre>#define EEPROM_INIT_NOW</pre>
</details>
<details><summary>2065~: PLA預熱參數</summary>
    <pre>
    #define PREHEAT_1_LABEL       "PLA"
    #define PREHEAT_1_TEMP_HOTEND 185
    #define PREHEAT_1_TEMP_BED     60
    #define PREHEAT_1_TEMP_CHAMBER 35
    #define PREHEAT_1_FAN_SPEED     0
    </pre>
</details>
<details><summary>2087 : 噴頭自動泊位</summary>
<pre>#define NOZZLE_PARK_FEATURE</pre>
</details>

<details><summary>2264 : LCD 顯示語系 zh_TW</summary>
<pre>#define LCD_LANGUAGE zh_TW</pre>
</details>
<details><summary>2303 : 啟用SD卡</summary>
    <pre>#define SDSUPPORT</pre>
</details>
<details><summary>2639 : LCD顯示屏模組</summary>
<pre>#define MKS_MINI_12864_V3</pre>
</details>
<details><summary>3099 ： 彩光模式</summary>
    <pre>
    #define NEOPIXEL_LED
    #if ENABLED(NEOPIXEL_LED)
    #define NEOPIXEL_TYPE          NEO_RGB 
    </pre>
</details>

---
<br>

## Configuation_adv.h

<details><summary>
    1282 :
    啟用 Probe偏移量精靈
    </summary>
    <pre>
    #define PROBE_OFFSET_WIZARD       
    #if ENABLED(PROBE_OFFSET_WIZARD)
        #define PROBE_OFFSET_WIZARD_START_Z -4.0
        //#define PROBE_OFFSET_WIZARD_XY_POS { X_CENTER, Y_CENTER }
    </pre>
</details>

<details><summary>
    1364 : 
    禁用 LED控制功能表
    </summary>
    <pre>
        //#define LED_CONTROL_MENU
    </pre>
</details>

<details><summary>
    2513 : 
    啟用 進階暫停參數
    </summary>
    <pre>#define ADVANCED_PAUSE_FEATURE</pre>
</details>

<details><summary>
    2704~
    : TMC SPI/UART 馬達參數
    800mA, 32 microsteps
    </summary>
    <pre>
#if HAS_TRINAMIC_CONFIG

  #define HOLD_MULTIPLIER    0.5  // Scales down the holding current from run current

  /**
   * Interpolate microsteps to 256
   * Override for each driver with <driver>_INTERPOLATE settings below
   */
  #define INTERPOLATE      true

  #if AXIS_IS_TMC(X)
    #define X_CURRENT       800        // (mA) RMS current. Multiply by 1.414 for peak current.
    #define X_CURRENT_HOME  X_CURRENT  // (mA) RMS current for sensorless homing
    #define X_MICROSTEPS     32        // 0..256
    #define X_RSENSE          0.11
    #define X_CHAIN_POS      -1        // -1..0: Not chained. 1: MCU MOSI connected. 2: Next in chain, ...
    //#define X_INTERPOLATE  true      // Enable to override 'INTERPOLATE' for the X axis
    //#define X_HOLD_MULTIPLIER 0.5    // Enable to override 'HOLD_MULTIPLIER' for the X axis
  #endif

  #if AXIS_IS_TMC(Y)
    #define Y_CURRENT       800
    #define Y_CURRENT_HOME  Y_CURRENT
    #define Y_MICROSTEPS     32
    #define Y_RSENSE          0.11
    #define Y_CHAIN_POS      -1
    //#define Y_INTERPOLATE  true
    //#define Y_HOLD_MULTIPLIER 0.5
  #endif

  #if AXIS_IS_TMC(Z)
    #define Z_CURRENT       800
    #define Z_CURRENT_HOME  Z_CURRENT
    #define Z_MICROSTEPS     32
    #define Z_RSENSE          0.11
    #define Z_CHAIN_POS      -1
    //#define Z_INTERPOLATE  true
    //#define Z_HOLD_MULTIPLIER 0.5
  #endif

  #if AXIS_IS_TMC(E0)
    #define E0_CURRENT      800
    #define E0_MICROSTEPS    32
    #define E0_RSENSE         0.11
    #define E0_CHAIN_POS     -1
    //#define E0_INTERPOLATE true
    //#define E0_HOLD_MULTIPLIER 0.5
  #endif
    </pre>
</details>

<details><summary>
    2997
    : 馬達波型生成器參數 <strong><font color="red">24 V</font></strong>
    </summary>
    <pre>#define CHOPPER_TIMING  CHOPPER_DEFAULT_24V</pre>
</details>

<details><summary>
    3091~
    : 啟用 無感測器歸位
    Sensitivity X:100 Y: 80
    </summary>
    <pre>
    #define SENSORLESS_HOMING // StallGuard capable drivers only
        #define X_STALL_SENSITIVITY  100
        #define Y_STALL_SENSITIVITY  80
    </pre>
</details>

---
<br>

## \src\LCD\language_zh_TW.h
<details><summary>
    218~
    ： 修正顯示錯誤
    </summary>
    <pre>
  LSTR MSG_MOVE_X                         = _UxGT("Move X");     // "Move X"
  LSTR MSG_MOVE_Y                         = _UxGT("Move Y");     // "Move Y"
  LSTR MSG_MOVE_Z                         = _UxGT("Move Z");     // "Move Z"
  LSTR MSG_MOVE_N                         = _UxGT("Move @");     // "Move @"
    </pre>
</details>

## \src\gcode\calibrate\G28.cpp
[MKS Robin E3D V1.1 User manul](https://blog.csdn.net/gjy_skyblue/article/details/119418639?spm=1001.2014.3001.5501)
<details><summary>
    591 : 
    設置校正時自動調用調平數據 
    </summary>
    <pre>set_bed_leveling_enabled(true);</pre>
</details>