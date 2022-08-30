# Marlin 2  - for Prusa i3 MK3 w. MKS Robin E3
### Based on Marlin 2.0 LST
[Marlin 2.0.9.5](https://github.com/MarlinFirmware/Marlin/tree/2.0.9.5)
<br>
<br>


## **Edit Note**
---
## Configuration.h
<details><summary>63 : �պA�@��</summary>
    �֧�F�o���ɮ�
</details>
<details><summary>64 : �ϥΫȨ�ƪ����ɮ�</summary>
    <pre>#define CUSTOM_VERSION_FILE Version.h</pre>
</details>
<details><summary>90 : �D�O���� BOARD_MKS_ROBIN_E3D_V1_1</summary>
    <pre>#define MOTHERBOARD BOARD_MKS_ROBIN_E3D_V1_1</pre>
</details>
<details><summary>101 : �ǦC�� 1</summary>
    <pre>#define SERIAL_PORT 1</pre>
</details>
<details><summary>137 : �Ȩ�ƾ����W�� "Felix Robin Prusa"</summary>
    <pre>#define CUSTOM_MACHINE_NAME "Felix Robin Prusa"</pre>
</details>
<details><summary>159~ : �X�ʾ����� TMC2209</summary>
    <pre>
    #define X_DRIVER_TYPE  TMC2209
    #define Y_DRIVER_TYPE  TMC2209
    #define Z_DRIVER_TYPE  TMC2209
    #define E0_DRIVER_TYPE TMC2209
    </pre>
</details>
<details><summary>511~ : �ū׷P����  1: EPCOS thermistors</summary>
    <pre>
    #define TEMP_SENSOR_0 1
    #define TEMP_SENSOR_BED 1
    </pre>
</details>
<details><summary>1087 : Steps/mm (200,200,800,283)</summary>
    <pre>#define DEFAULT_AXIS_STEPS_PER_UNIT   { 200, 200, 800, 283 }</pre>
</details>
<details><summary>1094 : �̤j�t�� { 600, 600, 30, 80 }</summary>
    <pre>#define DEFAULT_MAX_FEEDRATE          { 600, 600, 30, 80 }</pre>
</details>
<details><summary>1190~ : Z�k��ϥ�probe</summary>
    <pre>
    //#define Z_MIN_PROBE_USES_Z_MIN_ENDSTOP_PIN
    #define USE_PROBE_FOR_Z_HOMING
    </pre>
</details>   
<details><summary>1210 : Z�bProbe�}��  PB1</summary>
    <pre>#define Z_MIN_PROBE_PIN PB1</pre>
</details>
<details><summary>1320 : Probe���� FIX_MOUNTED_PROBE</summary>
    <pre>#define FIX_MOUNTED_PROBE</pre>
</details>
<details><summary>1529~ : �U�b��V�w�q</summary>
    <pre>
    #define INVERT_X_DIR true
    #define INVERT_Y_DIR true
    #define INVERT_Z_DIR false
    </pre>
</details>
<details><summary>1577~ : �����ɤئT</summary>
    <pre>
    #define X_BED_SIZE 230
    #define Y_BED_SIZE 210
    </pre>
</details>
<details><summary>1581~: �k����{�d�� �۹�󭭦쾹��m</summary>
    <pre>
    #define X_MIN_POS -5
    #define Y_MIN_POS -5
    #define Z_MIN_POS 1
    #define X_MAX_POS X_BED_SIZE
    #define Y_MAX_POS Y_BED_SIZE
    #define Z_MAX_POS 200
    </pre>
</details>
<details><summary><strong>1642 : �u�ƥκ��˴�  <font color=RED>N/A></font></strong></summary>
    <pre>#define FILAMENT_RUNOUT_SENSOR</pre>
</details>
<details><summary>1742~ : �۰ʼ��ɥ��x�շ� AUTO_BED_LEVELING_BILINEAR </summary>
    <pre>
    //#define AUTO_BED_LEVELING_3POINT
    //#define AUTO_BED_LEVELING_LINEAR
    #define AUTO_BED_LEVELING_BILINEAR
    //#define AUTO_BED_LEVELING_UBL
    //#define MESH_BED_LEVELING
    </pre>
</details>
<details><summary>1945 : Z �w���k��, �קKZ�b���ɤ��~�k��</summary>
    <pre>#define Z_SAFE_HOMING</pre>
</details>
<details><summary>1953 : �k��t�� : 3000, 3000, 2400</summary>
    <pre>#define HOMING_FEEDRATE_MM_M { (50*60), (50*60), (400*60) }</pre>
</details>
<details><summary>2030 : �ϥ�EEPROM�s�]�w��</summary>
    <pre>#define EEPROM_SETTINGS</pre>
</details>
<details><summary>2065~: PLA�w���Ѽ�</summary>
    <pre>
    #define PREHEAT_1_LABEL       "PLA"
    #define PREHEAT_1_TEMP_HOTEND 185
    #define PREHEAT_1_TEMP_BED     60
    #define PREHEAT_1_TEMP_CHAMBER 35
    #define PREHEAT_1_FAN_SPEED     0
    </pre>
</details>
<details><summary>


