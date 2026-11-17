# 中兴 G7615 / G7611 工具包

配套文章：[中兴 G7615 / G7611 开 Telnet、改地区与 OLT 模式](https://xiaozou123.cn/zte-g7615-g7611-telnet-region-olt/)

G7615 是 XG-PON 万兆网关，G7611 是同代的另一条产品线。这个包里东西最多：开 T、改地区、改 OLT 模式、分区备份与刷写。

## 目录

- `zteOnu/`：开源命令行开 T 工具（zteOnu 0.0.6-pre），`--telnet` 一步开
- `olt_tool_*`：三个版本的「一键改 OLT 模式」工具，分别对应 G7611&G7615 通用版、联通版、G7615v2 电信版
- `firmware_tool/`：移动版 G7615v1 固件更新工具
- `docs/`：四份原始命令文档，含区域码表、分区表、备份与刷写命令
- `common/`：ZTelnet、zte_factroymode、ztecfg、factorymode_crack、tftpd64

## Releases

`CMCC_7615v1_kernel_P2N21.bin`、`CMCC_7615v1_osgi_P2N21.bin`、`CMCC_7615v1_uboot_P2N21.bin`、`7615V2_kernel_CU.bin`。

## 风险提示

分区刷写（`nand kerase` / `nand kwrite`）会直接擦写 NAND，命令里写错 mtd 编号就救不回来。`docs/` 里的分区表来自一台真实设备，型号和固件不同就要重新 `cat /proc/mtd`，不要照抄。

## 文件与 SHA256

| 文件 | 字节 |
|---|---|
| `common/ZTelnet v1.0.5.exe` | 9,729,169 |
| `common/factorymode_crack.exe` | 872,448 |
| `common/tftpd64.exe` | 343,040 |
| `common/zte_factroymode.exe` | 9,840,829 |
| `common/ztecfg.exe` | 7,037,223 |
| `common/说明.txt` | 441 |
| `docs/G7615(F7607P)万兆光猫telnet命令.txt` | 3,689 |
| `docs/G7615V2_开telnet与固化.txt` | 2,810 |
| `docs/G7615_F7607P_通用telnet命令.txt` | 3,592 |
| `docs/G7615使用telnet命令备份与刷写固件的方法.txt` | 3,947 |
| `docs/G7615光猫telnet命令.txt` | 3,203 |
| `firmware_tool/移动版中兴G7615v1固件更新工具.exe` | 14,145,024 |
| `olt_tool_G7611_G7615/App/ClientConfigUI65U.dll` | 888,320 |
| `olt_tool_G7611_G7615/App/CommonUI65U.dll` | 260,608 |
| `olt_tool_G7611_G7615/App/Config/ButtonBar.ini` | 135 |
| `olt_tool_G7611_G7615/App/Config/Color Schemes.ini` | 1,885 |
| `olt_tool_G7611_G7615/App/Config/Global.ini` | 9,910 |
| `olt_tool_G7611_G7615/App/Config/SCRTMenuToolbar.ini` | 5,588 |
| `olt_tool_G7611_G7615/App/Config/Sessions/Default.ini` | 8,806 |
| `olt_tool_G7611_G7615/App/ConnectDialog65U.dll` | 435,200 |
| `olt_tool_G7611_G7615/App/MFC90ENU.dll` | 54,272 |
| `olt_tool_G7611_G7615/App/Microsoft.VC80.CRT.manifest` | 1,869 |
| `olt_tool_G7611_G7615/App/Microsoft.VC90.CRT.manifest` | 1,860 |
| `olt_tool_G7611_G7615/App/Microsoft.VC90.MFC.manifest` | 2,357 |
| `olt_tool_G7611_G7615/App/Microsoft.VC90.MFCLOC.manifest` | 5,377 |
| `olt_tool_G7611_G7615/App/Ont.dll` | 3,391,488 |
| `olt_tool_G7611_G7615/App/Telnet.dll` | 206,336 |
| `olt_tool_G7611_G7615/App/mfc90u.dll` | 3,780,424 |
| `olt_tool_G7611_G7615/App/msvcp80.dll` | 548,864 |
| `olt_tool_G7611_G7615/App/msvcp90.dll` | 569,664 |
| `olt_tool_G7611_G7615/App/msvcr80.dll` | 626,688 |
| `olt_tool_G7611_G7615/App/msvcr90.dll` | 653,120 |
| `olt_tool_G7611_G7615/中兴G7611&G7615一键改OLT模式工具.exe` | 3,096,576 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/ClientConfigUI65U.dll` | 888,320 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/CommonUI65U.dll` | 260,608 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Config/ButtonBar.ini` | 135 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Config/Color Schemes.ini` | 1,885 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Config/Global.ini` | 9,910 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Config/SCRTMenuToolbar.ini` | 5,588 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Config/Sessions/Default.ini` | 8,806 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/ConnectDialog65U.dll` | 435,200 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/MFC90ENU.dll` | 54,272 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Microsoft.VC80.CRT.manifest` | 1,869 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Microsoft.VC90.CRT.manifest` | 1,860 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Microsoft.VC90.MFC.manifest` | 2,357 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Microsoft.VC90.MFCLOC.manifest` | 5,377 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Ont.dll` | 3,392,000 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Telnet.dll` | 206,336 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/mfc90u.dll` | 3,780,424 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/msvcp80.dll` | 548,864 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/msvcp90.dll` | 569,664 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/msvcr80.dll` | 626,688 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/msvcr90.dll` | 653,120 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/Bin/MyHash.exe` | 623,104 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/Bin/MyHash.ini` | 169 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/Bin/MyHashExt.dll` | 305,664 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/Bin/hash.txt` | 106 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/中兴G7615v2电信一键改OLT模式教程.png` | 1,833,532 |
| `olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/中兴G7615v2电信版一键刷联通改Olt工具-恩山免费版.exe` | 3,059,712 |
| `olt_tool_unicom/App/ClientConfigUI65U.dll` | 888,320 |
| `olt_tool_unicom/App/CommonUI65U.dll` | 260,608 |
| `olt_tool_unicom/App/Config/ButtonBar.ini` | 135 |
| `olt_tool_unicom/App/Config/Color Schemes.ini` | 1,885 |
| `olt_tool_unicom/App/Config/Global.ini` | 9,910 |
| `olt_tool_unicom/App/Config/SCRTMenuToolbar.ini` | 5,588 |
| `olt_tool_unicom/App/Config/Sessions/Default.ini` | 8,806 |
| `olt_tool_unicom/App/ConnectDialog65U.dll` | 435,200 |
| `olt_tool_unicom/App/MFC90ENU.dll` | 54,272 |
| `olt_tool_unicom/App/Microsoft.VC80.CRT.manifest` | 1,869 |
| `olt_tool_unicom/App/Microsoft.VC90.CRT.manifest` | 1,860 |
| `olt_tool_unicom/App/Microsoft.VC90.MFC.manifest` | 2,357 |
| `olt_tool_unicom/App/Microsoft.VC90.MFCLOC.manifest` | 5,377 |
| `olt_tool_unicom/App/Ont.dll` | 3,391,488 |
| `olt_tool_unicom/App/Telnet.dll` | 206,336 |
| `olt_tool_unicom/App/mfc90u.dll` | 3,780,424 |
| `olt_tool_unicom/App/msvcp80.dll` | 548,864 |
| `olt_tool_unicom/App/msvcp90.dll` | 569,664 |
| `olt_tool_unicom/App/msvcr80.dll` | 626,688 |
| `olt_tool_unicom/App/msvcr90.dll` | 653,120 |
| `olt_tool_unicom/中兴G7611&G7615一键改OLT模式工具.exe` | 3,096,576 |
| `zteOnu/LICENSE` | 34,523 |
| `zteOnu/README.md` | 37 |
| `zteOnu/zteOnu.exe` | 7,940,608 |

```
c6b0fc3056864024ab0b153cc1f8aabd2d60ef4d61a3abde19adf1d122b5743f  common/ZTelnet v1.0.5.exe
e5fa3ca8a74a768c58abe7a0e552bbd66276353804604cbaa6c2479b95b9d702  common/factorymode_crack.exe
2f5de838cf3079723f1697e5fac2f75fad4b98cd81b165f87cdfa99ded22d801  common/tftpd64.exe
7fae6d52429eca484d75f51d9d3a2fcb03b790a8cd40c6885685b7d8e34926b8  common/zte_factroymode.exe
a14be5d00516fc8ca950e97347e4f6e3f535f354254542f746739407aa9e3f46  common/ztecfg.exe
06726ff1e1f040eeea221d528bb9478dd1964e89c2cd63455161651ffe4707f0  common/说明.txt
fdad20aaedf4594392e6b3ef46b1eab1b98defd79a337721626cf278578e6fb2  docs/G7615(F7607P)万兆光猫telnet命令.txt
924c7b662584b955e44de7b8132810b67cb2ddcbb88c20ecca733f1054b299c5  docs/G7615V2_开telnet与固化.txt
596df144ab372a30ac4b93f2f1453fe0e4b7353a9a7a447b5ee4081b1f96cb0c  docs/G7615_F7607P_通用telnet命令.txt
a534d02637d467cc3d9633143a03ddb632a27916cc40fdb9f465f6729def276c  docs/G7615使用telnet命令备份与刷写固件的方法.txt
5468734dbcf7663e7a5d27d411a0dd65f7eac67ae992490e66c77d2ee9b282e9  docs/G7615光猫telnet命令.txt
56957408b28de98876253b0cf5d089936d87363dd4ae2e1260ca430482572ae2  firmware_tool/移动版中兴G7615v1固件更新工具.exe
eb9f413eec1c77ae168d320ad58591fa249af6fd0778a90193cd6e3c01a7c692  olt_tool_G7611_G7615/App/ClientConfigUI65U.dll
fe4d63d26005e0a24b90a3939b9606aecd5e17971bbcf7e7100e316f731ab8bb  olt_tool_G7611_G7615/App/CommonUI65U.dll
496cb3c8a6677a93d9821f0346fb2adb9152ef959f23d224607833ed63a304ba  olt_tool_G7611_G7615/App/Config/ButtonBar.ini
3f77b3c7fe57a9d645fe6f5fe92b134404318bb2466452bd6f22c24d82862696  olt_tool_G7611_G7615/App/Config/Color Schemes.ini
aa6a0df19b678af43196ed3b0007f3280eb91f1a26c5182b8bb9bc2c5e494f3f  olt_tool_G7611_G7615/App/Config/Global.ini
dc0ae456286dd151102652ef3166ede5d1c1e81bec6dbdd9b7b2f893d5567303  olt_tool_G7611_G7615/App/Config/SCRTMenuToolbar.ini
94ca771b694153fe44d05eec42cb202f70d967264cb60bc8f1219fb60664a0de  olt_tool_G7611_G7615/App/Config/Sessions/Default.ini
bf639208e62fc7bf683f11cebdeea7e123b60e2f8ef2f8f5e1d4846b988a4cc7  olt_tool_G7611_G7615/App/ConnectDialog65U.dll
a3e2c202e556791dee9d18962ca6780761b415313bcd104c2e621ba4089801a4  olt_tool_G7611_G7615/App/MFC90ENU.dll
17ad1a64ba1c382abf89341b40950f9b31f95015c6b0d3e25925bfebc1b53eb5  olt_tool_G7611_G7615/App/Microsoft.VC80.CRT.manifest
03d0776812368478ce60e8160ec3c6938782db1832f5cb53b7842e5840f9dbc5  olt_tool_G7611_G7615/App/Microsoft.VC90.CRT.manifest
1fed2074ab9f90d9fccc5a49b6aa42c917674c2b5c7b1bb93fb67b0e0c944818  olt_tool_G7611_G7615/App/Microsoft.VC90.MFC.manifest
81e13dc44e21fca2b095e82c34294c199d37428f32de36d5ffa6cd3b54f88d7b  olt_tool_G7611_G7615/App/Microsoft.VC90.MFCLOC.manifest
0b1482ceb46cf387f02dcc8f39678e324f3ac9cab8254361b87277057d3a1062  olt_tool_G7611_G7615/App/Ont.dll
8d3a082d5cfa57f01cbd143e7bfff97d47ae5d99714ac450895afd8a2214772e  olt_tool_G7611_G7615/App/Telnet.dll
314ef0e1c636ac553c0e09f992b34573da4a89accb759bda27335e8125c08e35  olt_tool_G7611_G7615/App/mfc90u.dll
2026f3c4f830dff6883b88e2647272a52a132f25eb42c0d423e36b3f65a94d08  olt_tool_G7611_G7615/App/msvcp80.dll
4608beedd8cf9c3fc5ab03716b4ab6f01c7b7d65a7c072af04f514ffb0e02d01  olt_tool_G7611_G7615/App/msvcp90.dll
02bdde38e4c6bd795a092d496b8d6060cdbe71e22ef4d7a204e3050c1be44fa9  olt_tool_G7611_G7615/App/msvcr80.dll
e16bc9b66642151de612ee045c2810ca6146975015bd9679a354567f56da2099  olt_tool_G7611_G7615/App/msvcr90.dll
62079406906ca46e1c65e2da03a8e90a2e433ec5e1bc21de4ee59253aa140373  olt_tool_G7611_G7615/中兴G7611&G7615一键改OLT模式工具.exe
eb9f413eec1c77ae168d320ad58591fa249af6fd0778a90193cd6e3c01a7c692  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/ClientConfigUI65U.dll
fe4d63d26005e0a24b90a3939b9606aecd5e17971bbcf7e7100e316f731ab8bb  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/CommonUI65U.dll
496cb3c8a6677a93d9821f0346fb2adb9152ef959f23d224607833ed63a304ba  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Config/ButtonBar.ini
3f77b3c7fe57a9d645fe6f5fe92b134404318bb2466452bd6f22c24d82862696  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Config/Color Schemes.ini
15c22dfcee9caa44538e2069e3228938b5282912fc2ea3a1d5daf32069b0ee3b  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Config/Global.ini
dc0ae456286dd151102652ef3166ede5d1c1e81bec6dbdd9b7b2f893d5567303  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Config/SCRTMenuToolbar.ini
94ca771b694153fe44d05eec42cb202f70d967264cb60bc8f1219fb60664a0de  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Config/Sessions/Default.ini
bf639208e62fc7bf683f11cebdeea7e123b60e2f8ef2f8f5e1d4846b988a4cc7  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/ConnectDialog65U.dll
a3e2c202e556791dee9d18962ca6780761b415313bcd104c2e621ba4089801a4  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/MFC90ENU.dll
17ad1a64ba1c382abf89341b40950f9b31f95015c6b0d3e25925bfebc1b53eb5  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Microsoft.VC80.CRT.manifest
03d0776812368478ce60e8160ec3c6938782db1832f5cb53b7842e5840f9dbc5  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Microsoft.VC90.CRT.manifest
1fed2074ab9f90d9fccc5a49b6aa42c917674c2b5c7b1bb93fb67b0e0c944818  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Microsoft.VC90.MFC.manifest
81e13dc44e21fca2b095e82c34294c199d37428f32de36d5ffa6cd3b54f88d7b  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Microsoft.VC90.MFCLOC.manifest
fa1c769afddf0411090338cbfb682bb237f4af3706eff54a943e4654fc2e57ed  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Ont.dll
8d3a082d5cfa57f01cbd143e7bfff97d47ae5d99714ac450895afd8a2214772e  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/Telnet.dll
314ef0e1c636ac553c0e09f992b34573da4a89accb759bda27335e8125c08e35  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/mfc90u.dll
2026f3c4f830dff6883b88e2647272a52a132f25eb42c0d423e36b3f65a94d08  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/msvcp80.dll
4608beedd8cf9c3fc5ab03716b4ab6f01c7b7d65a7c072af04f514ffb0e02d01  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/msvcp90.dll
02bdde38e4c6bd795a092d496b8d6060cdbe71e22ef4d7a204e3050c1be44fa9  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/msvcr80.dll
e16bc9b66642151de612ee045c2810ca6146975015bd9679a354567f56da2099  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/App/msvcr90.dll
d509de10a38ee4d96b7f8a6461ba2630762ce238763fa0e0aec7df590f00d0b6  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/Bin/MyHash.exe
0b5345c52088adf72efe4a8e799fe4f09e65480c4571c03ed5562d66578f7d01  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/Bin/MyHash.ini
c1556480bf3e26d53c8d349abb7d534c5b6e441f7cece408d18d0009545a19a1  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/Bin/MyHashExt.dll
be0e6fd7a886fa2f4957701e47fc9588b58d973423164c4e0a939e7aa54715c3  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/Bin/hash.txt
3a05c3259d2132b8d87b8614b72da25021c2419132f1f331c89359059440b676  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/中兴G7615v2电信一键改OLT模式教程.png
ef5a55be1bb6ca5b2cf0c9d04849c61057814a5b81e7df5f2ee6382b885841d5  olt_tool_G7615v2_telecom/中兴G7615v2电信一键改OLT模式工具/中兴G7615v2电信版一键刷联通改Olt工具-恩山免费版.exe
eb9f413eec1c77ae168d320ad58591fa249af6fd0778a90193cd6e3c01a7c692  olt_tool_unicom/App/ClientConfigUI65U.dll
fe4d63d26005e0a24b90a3939b9606aecd5e17971bbcf7e7100e316f731ab8bb  olt_tool_unicom/App/CommonUI65U.dll
496cb3c8a6677a93d9821f0346fb2adb9152ef959f23d224607833ed63a304ba  olt_tool_unicom/App/Config/ButtonBar.ini
3f77b3c7fe57a9d645fe6f5fe92b134404318bb2466452bd6f22c24d82862696  olt_tool_unicom/App/Config/Color Schemes.ini
aa6a0df19b678af43196ed3b0007f3280eb91f1a26c5182b8bb9bc2c5e494f3f  olt_tool_unicom/App/Config/Global.ini
dc0ae456286dd151102652ef3166ede5d1c1e81bec6dbdd9b7b2f893d5567303  olt_tool_unicom/App/Config/SCRTMenuToolbar.ini
94ca771b694153fe44d05eec42cb202f70d967264cb60bc8f1219fb60664a0de  olt_tool_unicom/App/Config/Sessions/Default.ini
bf639208e62fc7bf683f11cebdeea7e123b60e2f8ef2f8f5e1d4846b988a4cc7  olt_tool_unicom/App/ConnectDialog65U.dll
a3e2c202e556791dee9d18962ca6780761b415313bcd104c2e621ba4089801a4  olt_tool_unicom/App/MFC90ENU.dll
17ad1a64ba1c382abf89341b40950f9b31f95015c6b0d3e25925bfebc1b53eb5  olt_tool_unicom/App/Microsoft.VC80.CRT.manifest
03d0776812368478ce60e8160ec3c6938782db1832f5cb53b7842e5840f9dbc5  olt_tool_unicom/App/Microsoft.VC90.CRT.manifest
1fed2074ab9f90d9fccc5a49b6aa42c917674c2b5c7b1bb93fb67b0e0c944818  olt_tool_unicom/App/Microsoft.VC90.MFC.manifest
81e13dc44e21fca2b095e82c34294c199d37428f32de36d5ffa6cd3b54f88d7b  olt_tool_unicom/App/Microsoft.VC90.MFCLOC.manifest
0b1482ceb46cf387f02dcc8f39678e324f3ac9cab8254361b87277057d3a1062  olt_tool_unicom/App/Ont.dll
8d3a082d5cfa57f01cbd143e7bfff97d47ae5d99714ac450895afd8a2214772e  olt_tool_unicom/App/Telnet.dll
314ef0e1c636ac553c0e09f992b34573da4a89accb759bda27335e8125c08e35  olt_tool_unicom/App/mfc90u.dll
2026f3c4f830dff6883b88e2647272a52a132f25eb42c0d423e36b3f65a94d08  olt_tool_unicom/App/msvcp80.dll
4608beedd8cf9c3fc5ab03716b4ab6f01c7b7d65a7c072af04f514ffb0e02d01  olt_tool_unicom/App/msvcp90.dll
02bdde38e4c6bd795a092d496b8d6060cdbe71e22ef4d7a204e3050c1be44fa9  olt_tool_unicom/App/msvcr80.dll
e16bc9b66642151de612ee045c2810ca6146975015bd9679a354567f56da2099  olt_tool_unicom/App/msvcr90.dll
62079406906ca46e1c65e2da03a8e90a2e433ec5e1bc21de4ee59253aa140373  olt_tool_unicom/中兴G7611&G7615一键改OLT模式工具.exe
8486a10c4393cee1c25392769ddd3b2d6c242d6ec7928e1414efff7dfb2f07ef  zteOnu/LICENSE
07b5e5c709df641420028a2f3d1fc3e6c4ee991df76c45190cf66a417f5b62dc  zteOnu/README.md
81d4fadfbaf663b2a78a48094a6b253eb553873c4d2e87f8878be127fd5c1481  zteOnu/zteOnu.exe
```

## 相关仓库

同品牌其它机型，命令体系相近，排障时可以互相参照；每个仓库开头都对应一篇文章：

- [中兴 F650 / F1855V2 工具包](https://github.com/dellzou/ZTE_F650_F1855V2_Flashing_Software_and_Tutorial)：中兴 F650 / F1855V2，天翼网关 4.0 开 Telnet
- [中兴 F673AV9 / F7015TV3 / F7610M 工具包](https://github.com/dellzou/ZTE_F673AV9_F7015TV3_F7610M_Flashing_Software_and_Tutorial)：中兴 F673AV9 / F7015TV3 / F7610M，一套命令通吃
- [中兴 F7607P 工具包](https://github.com/dellzou/ZTE_F7607P_Flashing_Software_and_Tutorial)：中兴 F7607P，改地区与电信版固件
- [中兴 G7610 工具包](https://github.com/dellzou/ZTE_G7610_Flashing_Software_and_Tutorial)：中兴 G7610，工厂模式、setmac 改码、配置解密

## 免责声明

工具与固件均来自公开维修资料，仅供自有设备维修与学习使用。刷机有风险，操作前先备份，后果自负。
