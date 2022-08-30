# Marlin 2  - for Prusa i3 MK3 w. MKS Robin E3
### Based on Marlin 2.0 LST
[Marlin 2.0.9.5](https://github.com/MarlinFirmware/Marlin/tree/2.0.9.5)
<br>
<br>


## **Edit Note**
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
<details><summary>1087 : Steps/mm (200,200,800,283)</summary>
    <pre>#define DEFAULT_AXIS_STEPS_PER_UNIT   { 200, 200, 800, 283 }</pre>
</details>
<details><summary>1094 : 最大速度 { 600, 600, 30, 80 }</summary>
    <pre>#define DEFAULT_MAX_FEEDRATE          { 600, 600, 30, 80 }</pre>
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
<details><summary>1320 : Probe型式 FIX_MOUNTED_PROBE</summary>
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
<details><summary>1581~: 歸位後行程範圍 相對於限位器位置</summary>
    <pre>
    #define X_MIN_POS -5
    #define Y_MIN_POS -5
    #define Z_MIN_POS 1
    #define X_MAX_POS X_BED_SIZE
    #define Y_MAX_POS Y_BED_SIZE
    #define Z_MAX_POS 200
    </pre>
</details>
<details><summary><strong>1642 : 線料用盡檢測  <font color=RED>N/A></font></strong></summary>
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
    <pre>#define HOMING_FEEDRATE_MM_M { (50*60), (50*60), (400*60) }</pre>
</details>
<details><summary>2030 : 使用EEPROM存設定值</summary>
    <pre>#define EEPROM_SETTINGS</pre>
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
<details><summary>


