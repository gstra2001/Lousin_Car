cmake_minimum_required(VERSION 3.17)
project(HITSIC_MK66F18)

set(CMAKE_CXX_STANDARD 14)

include_directories(deprecated)
include_directories(deprecated/module)
include_directories(HITSIC_MK66F18_MCUX/board)
include_directories(HITSIC_MK66F18_MCUX/CMSIS)
include_directories(HITSIC_MK66F18_MCUX/component/lists)
include_directories(HITSIC_MK66F18_MCUX/component/osa)
include_directories(HITSIC_MK66F18_MCUX/component/serial_manager)
include_directories(HITSIC_MK66F18_MCUX/component/uart)
include_directories(HITSIC_MK66F18_MCUX/device)
include_directories(HITSIC_MK66F18_MCUX/drivers)
include_directories(HITSIC_MK66F18_MCUX/fatfs/source)
include_directories(HITSIC_MK66F18_MCUX/fatfs/source/fsl_ram_disk)
include_directories(HITSIC_MK66F18_MCUX/fatfs/source/fsl_sd_disk)
include_directories(HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18)
include_directories(HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/extlib_port/CmBacktrace-1.4.0)
include_directories(HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/extlib_port/CmBacktrace-1.4.0/cm_backtrace)
include_directories(HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/extlib_port/EasyFlash-4.0.0/easyflash/port)
include_directories(HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers)
include_directories(HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/deprecated)
include_directories(HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible)
include_directories(HITSIC_MK66F18_MCUX/HITSIC_Module/deprecated)
include_directories(HITSIC_MK66F18_MCUX/HITSIC_Module/utilities)
include_directories(HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/CmBacktrace-1.4.0/cm_backtrace)
include_directories(HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/inc)
include_directories(HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/plugins/types)
include_directories(HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/plugins/types/struct2json/inc)
include_directories(HITSIC_MK66F18_MCUX/HITSIC_Module/utilities_test)
include_directories(HITSIC_MK66F18_MCUX/osa)
include_directories(HITSIC_MK66F18_MCUX/sdmmc/host)
include_directories(HITSIC_MK66F18_MCUX/sdmmc/inc)
include_directories(HITSIC_MK66F18_MCUX/sdmmc/osa)
include_directories(HITSIC_MK66F18_MCUX/source)
include_directories(HITSIC_MK66F18_MCUX/utilities)

add_executable(HITSIC_MK66F18
        deprecated/module/drv_disp_lcd240.cpp
        deprecated/module/drv_disp_lcd240.hpp
        deprecated/module/drv_extInt.cpp
        deprecated/module/drv_extInt.hpp
        deprecated/module/drv_motor.cpp
        deprecated/module/drv_motor.hpp
        deprecated/module/drv_pitmgr.cpp
        deprecated/module/drv_pitmgr.hpp
        deprecated/module/drv_uartmgr.cpp
        deprecated/module/drv_uartmgr.hpp
        deprecated/module/rte_common.cpp
        deprecated/module/rte_common.hpp
        deprecated/include.hpp
        deprecated/retarget_itm.c
        deprecated/semihost_hardfault.c
        HITSIC_MK66F18_MCUX/board/board.c
        HITSIC_MK66F18_MCUX/board/board.h
        HITSIC_MK66F18_MCUX/board/clock_config.c
        HITSIC_MK66F18_MCUX/board/clock_config.h
        HITSIC_MK66F18_MCUX/board/peripherals.c
        HITSIC_MK66F18_MCUX/board/peripherals.h
        HITSIC_MK66F18_MCUX/board/pin_mux.c
        HITSIC_MK66F18_MCUX/board/pin_mux.h
        HITSIC_MK66F18_MCUX/board/sdmmc_config.c
        HITSIC_MK66F18_MCUX/board/sdmmc_config.h
        HITSIC_MK66F18_MCUX/CMSIS/arm_common_tables.h
        HITSIC_MK66F18_MCUX/CMSIS/arm_const_structs.h
        HITSIC_MK66F18_MCUX/CMSIS/arm_helium_utils.h
        HITSIC_MK66F18_MCUX/CMSIS/arm_math.h
        HITSIC_MK66F18_MCUX/CMSIS/arm_mve_tables.h
        HITSIC_MK66F18_MCUX/CMSIS/arm_vec_math.h
        HITSIC_MK66F18_MCUX/CMSIS/cachel1_armv7.h
        HITSIC_MK66F18_MCUX/CMSIS/cmsis_armcc.h
        HITSIC_MK66F18_MCUX/CMSIS/cmsis_armclang.h
        HITSIC_MK66F18_MCUX/CMSIS/cmsis_armclang_ltm.h
        HITSIC_MK66F18_MCUX/CMSIS/cmsis_compiler.h
        HITSIC_MK66F18_MCUX/CMSIS/cmsis_gcc.h
        HITSIC_MK66F18_MCUX/CMSIS/cmsis_iccarm.h
        HITSIC_MK66F18_MCUX/CMSIS/cmsis_version.h
        HITSIC_MK66F18_MCUX/CMSIS/core_armv81mml.h
        HITSIC_MK66F18_MCUX/CMSIS/core_armv8mbl.h
        HITSIC_MK66F18_MCUX/CMSIS/core_armv8mml.h
        HITSIC_MK66F18_MCUX/CMSIS/core_cm0.h
        HITSIC_MK66F18_MCUX/CMSIS/core_cm0plus.h
        HITSIC_MK66F18_MCUX/CMSIS/core_cm1.h
        HITSIC_MK66F18_MCUX/CMSIS/core_cm23.h
        HITSIC_MK66F18_MCUX/CMSIS/core_cm3.h
        HITSIC_MK66F18_MCUX/CMSIS/core_cm33.h
        HITSIC_MK66F18_MCUX/CMSIS/core_cm35p.h
        HITSIC_MK66F18_MCUX/CMSIS/core_cm4.h
        HITSIC_MK66F18_MCUX/CMSIS/core_cm55.h
        HITSIC_MK66F18_MCUX/CMSIS/core_cm7.h
        HITSIC_MK66F18_MCUX/CMSIS/core_sc000.h
        HITSIC_MK66F18_MCUX/CMSIS/core_sc300.h
        HITSIC_MK66F18_MCUX/CMSIS/mpu_armv7.h
        HITSIC_MK66F18_MCUX/CMSIS/mpu_armv8.h
        HITSIC_MK66F18_MCUX/CMSIS/pmu_armv8.h
        HITSIC_MK66F18_MCUX/CMSIS/tz_context.h
        HITSIC_MK66F18_MCUX/component/lists/generic_list.c
        HITSIC_MK66F18_MCUX/component/lists/generic_list.h
        HITSIC_MK66F18_MCUX/component/osa/fsl_os_abstraction.h
        HITSIC_MK66F18_MCUX/component/osa/fsl_os_abstraction_bm.c
        HITSIC_MK66F18_MCUX/component/osa/fsl_os_abstraction_bm.h
        HITSIC_MK66F18_MCUX/component/osa/fsl_os_abstraction_config.h
        HITSIC_MK66F18_MCUX/component/serial_manager/serial_manager.c
        HITSIC_MK66F18_MCUX/component/serial_manager/serial_manager.h
        HITSIC_MK66F18_MCUX/component/serial_manager/serial_port_internal.h
        HITSIC_MK66F18_MCUX/component/serial_manager/serial_port_uart.c
        HITSIC_MK66F18_MCUX/component/serial_manager/serial_port_uart.h
        HITSIC_MK66F18_MCUX/component/uart/lpuart_adapter.c
        HITSIC_MK66F18_MCUX/component/uart/uart.h
        HITSIC_MK66F18_MCUX/component/uart/uart_adapter.c
        HITSIC_MK66F18_MCUX/device/fsl_device_registers.h
        HITSIC_MK66F18_MCUX/device/MK66F18.h
        HITSIC_MK66F18_MCUX/device/MK66F18_features.h
        HITSIC_MK66F18_MCUX/device/system_MK66F18.c
        HITSIC_MK66F18_MCUX/device/system_MK66F18.h
        HITSIC_MK66F18_MCUX/drivers/fsl_adc16.c
        HITSIC_MK66F18_MCUX/drivers/fsl_adc16.h
        HITSIC_MK66F18_MCUX/drivers/fsl_cache.c
        HITSIC_MK66F18_MCUX/drivers/fsl_cache.h
        HITSIC_MK66F18_MCUX/drivers/fsl_clock.c
        HITSIC_MK66F18_MCUX/drivers/fsl_clock.h
        HITSIC_MK66F18_MCUX/drivers/fsl_cmp.c
        HITSIC_MK66F18_MCUX/drivers/fsl_cmp.h
        HITSIC_MK66F18_MCUX/drivers/fsl_cmt.c
        HITSIC_MK66F18_MCUX/drivers/fsl_cmt.h
        HITSIC_MK66F18_MCUX/drivers/fsl_common.c
        HITSIC_MK66F18_MCUX/drivers/fsl_common.h
        HITSIC_MK66F18_MCUX/drivers/fsl_crc.c
        HITSIC_MK66F18_MCUX/drivers/fsl_crc.h
        HITSIC_MK66F18_MCUX/drivers/fsl_dac.c
        HITSIC_MK66F18_MCUX/drivers/fsl_dac.h
        HITSIC_MK66F18_MCUX/drivers/fsl_dmamux.c
        HITSIC_MK66F18_MCUX/drivers/fsl_dmamux.h
        HITSIC_MK66F18_MCUX/drivers/fsl_dspi.c
        HITSIC_MK66F18_MCUX/drivers/fsl_dspi.h
        HITSIC_MK66F18_MCUX/drivers/fsl_dspi_edma.c
        HITSIC_MK66F18_MCUX/drivers/fsl_dspi_edma.h
        HITSIC_MK66F18_MCUX/drivers/fsl_edma.c
        HITSIC_MK66F18_MCUX/drivers/fsl_edma.h
        HITSIC_MK66F18_MCUX/drivers/fsl_enet.c
        HITSIC_MK66F18_MCUX/drivers/fsl_enet.h
        HITSIC_MK66F18_MCUX/drivers/fsl_ewm.c
        HITSIC_MK66F18_MCUX/drivers/fsl_ewm.h
        HITSIC_MK66F18_MCUX/drivers/fsl_flash.h
        HITSIC_MK66F18_MCUX/drivers/fsl_flexbus.c
        HITSIC_MK66F18_MCUX/drivers/fsl_flexbus.h
        HITSIC_MK66F18_MCUX/drivers/fsl_flexcan.c
        HITSIC_MK66F18_MCUX/drivers/fsl_flexcan.h
        HITSIC_MK66F18_MCUX/drivers/fsl_ftfx_adapter.h
        HITSIC_MK66F18_MCUX/drivers/fsl_ftfx_cache.c
        HITSIC_MK66F18_MCUX/drivers/fsl_ftfx_cache.h
        HITSIC_MK66F18_MCUX/drivers/fsl_ftfx_controller.c
        HITSIC_MK66F18_MCUX/drivers/fsl_ftfx_controller.h
        HITSIC_MK66F18_MCUX/drivers/fsl_ftfx_features.h
        HITSIC_MK66F18_MCUX/drivers/fsl_ftfx_flash.c
        HITSIC_MK66F18_MCUX/drivers/fsl_ftfx_flash.h
        HITSIC_MK66F18_MCUX/drivers/fsl_ftfx_flexnvm.c
        HITSIC_MK66F18_MCUX/drivers/fsl_ftfx_flexnvm.h
        HITSIC_MK66F18_MCUX/drivers/fsl_ftfx_utilities.h
        HITSIC_MK66F18_MCUX/drivers/fsl_ftm.c
        HITSIC_MK66F18_MCUX/drivers/fsl_ftm.h
        HITSIC_MK66F18_MCUX/drivers/fsl_gpio.c
        HITSIC_MK66F18_MCUX/drivers/fsl_gpio.h
        HITSIC_MK66F18_MCUX/drivers/fsl_i2c.c
        HITSIC_MK66F18_MCUX/drivers/fsl_i2c.h
        HITSIC_MK66F18_MCUX/drivers/fsl_i2c_edma.c
        HITSIC_MK66F18_MCUX/drivers/fsl_i2c_edma.h
        HITSIC_MK66F18_MCUX/drivers/fsl_llwu.c
        HITSIC_MK66F18_MCUX/drivers/fsl_llwu.h
        HITSIC_MK66F18_MCUX/drivers/fsl_lmem_cache.c
        HITSIC_MK66F18_MCUX/drivers/fsl_lmem_cache.h
        HITSIC_MK66F18_MCUX/drivers/fsl_lptmr.c
        HITSIC_MK66F18_MCUX/drivers/fsl_lptmr.h
        HITSIC_MK66F18_MCUX/drivers/fsl_lpuart.c
        HITSIC_MK66F18_MCUX/drivers/fsl_lpuart.h
        HITSIC_MK66F18_MCUX/drivers/fsl_lpuart_edma.c
        HITSIC_MK66F18_MCUX/drivers/fsl_lpuart_edma.h
        HITSIC_MK66F18_MCUX/drivers/fsl_pdb.c
        HITSIC_MK66F18_MCUX/drivers/fsl_pdb.h
        HITSIC_MK66F18_MCUX/drivers/fsl_pit.c
        HITSIC_MK66F18_MCUX/drivers/fsl_pit.h
        HITSIC_MK66F18_MCUX/drivers/fsl_pmc.c
        HITSIC_MK66F18_MCUX/drivers/fsl_pmc.h
        HITSIC_MK66F18_MCUX/drivers/fsl_port.h
        HITSIC_MK66F18_MCUX/drivers/fsl_rcm.c
        HITSIC_MK66F18_MCUX/drivers/fsl_rcm.h
        HITSIC_MK66F18_MCUX/drivers/fsl_rnga.c
        HITSIC_MK66F18_MCUX/drivers/fsl_rnga.h
        HITSIC_MK66F18_MCUX/drivers/fsl_rtc.c
        HITSIC_MK66F18_MCUX/drivers/fsl_rtc.h
        HITSIC_MK66F18_MCUX/drivers/fsl_sai.c
        HITSIC_MK66F18_MCUX/drivers/fsl_sai.h
        HITSIC_MK66F18_MCUX/drivers/fsl_sai_edma.c
        HITSIC_MK66F18_MCUX/drivers/fsl_sai_edma.h
        HITSIC_MK66F18_MCUX/drivers/fsl_sdhc.c
        HITSIC_MK66F18_MCUX/drivers/fsl_sdhc.h
        HITSIC_MK66F18_MCUX/drivers/fsl_sdramc.c
        HITSIC_MK66F18_MCUX/drivers/fsl_sdramc.h
        HITSIC_MK66F18_MCUX/drivers/fsl_sim.c
        HITSIC_MK66F18_MCUX/drivers/fsl_sim.h
        HITSIC_MK66F18_MCUX/drivers/fsl_smc.c
        HITSIC_MK66F18_MCUX/drivers/fsl_smc.h
        HITSIC_MK66F18_MCUX/drivers/fsl_sysmpu.c
        HITSIC_MK66F18_MCUX/drivers/fsl_sysmpu.h
        HITSIC_MK66F18_MCUX/drivers/fsl_tpm.c
        HITSIC_MK66F18_MCUX/drivers/fsl_tpm.h
        HITSIC_MK66F18_MCUX/drivers/fsl_tsi_v4.c
        HITSIC_MK66F18_MCUX/drivers/fsl_tsi_v4.h
        HITSIC_MK66F18_MCUX/drivers/fsl_uart.c
        HITSIC_MK66F18_MCUX/drivers/fsl_uart.h
        HITSIC_MK66F18_MCUX/drivers/fsl_uart_edma.c
        HITSIC_MK66F18_MCUX/drivers/fsl_uart_edma.h
        HITSIC_MK66F18_MCUX/drivers/fsl_vref.c
        HITSIC_MK66F18_MCUX/drivers/fsl_vref.h
        HITSIC_MK66F18_MCUX/drivers/fsl_wdog.c
        HITSIC_MK66F18_MCUX/drivers/fsl_wdog.h
        HITSIC_MK66F18_MCUX/fatfs/source/fsl_ram_disk/fsl_ram_disk.c
        HITSIC_MK66F18_MCUX/fatfs/source/fsl_ram_disk/fsl_ram_disk.h
        HITSIC_MK66F18_MCUX/fatfs/source/fsl_sd_disk/fsl_sd_disk.c
        HITSIC_MK66F18_MCUX/fatfs/source/fsl_sd_disk/fsl_sd_disk.h
        HITSIC_MK66F18_MCUX/fatfs/source/diskio.c
        HITSIC_MK66F18_MCUX/fatfs/source/diskio.h
        HITSIC_MK66F18_MCUX/fatfs/source/ff.c
        HITSIC_MK66F18_MCUX/fatfs/source/ff.h
        HITSIC_MK66F18_MCUX/fatfs/source/ffsystem.c
        HITSIC_MK66F18_MCUX/fatfs/source/ffunicode.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/extlib_port/CmBacktrace-1.4.0/cm_backtrace/cmb_cfg.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/extlib_port/CmBacktrace-1.4.0/cm_backtrace/cmb_def.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/extlib_port/EasyFlash-4.0.0/easyflash/port/ef_cfg.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/extlib_port/EasyFlash-4.0.0/easyflash/port/ef_port.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/deprecated/SmartCar_Beep.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/deprecated/SmartCar_Beep.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/deprecated/SmartCar_Boma.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/deprecated/SmartCar_Boma.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/deprecated/SmartCar_Key.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/deprecated/SmartCar_Key.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/deprecated/SmartCar_LED.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/deprecated/SmartCar_LED.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/deprecated/SmartCar_OLED.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/deprecated/SmartCar_OLED.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/deprecated/SmartCar_Systick.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/deprecated/SmartCar_Systick.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible/SmartCar_AD5206.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible/SmartCar_AD5206.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible/SmartCar_ADC.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible/SmartCar_ADC.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible/SmartCar_ADC_dma.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible/SmartCar_ADC_dma.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible/SmartCar_Camera.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible/SmartCar_Camera.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible/SmartCar_Pit.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible/SmartCar_Pit.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible/SmartCar_Sd.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible/SmartCar_Sd.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible/SmartCar_TF.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/incompatible/SmartCar_TF.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/drv_cam.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/drv_cam.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/drv_cam_def.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/include.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/SmartCar_Ftm.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/SmartCar_Ftm.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/SmartCar_Upload.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/SmartCar_Upload.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/SmartCar_Wdog.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/legacy_drivers/SmartCar_Wdog.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/app_menu_port.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/app_menu_port.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/drv_cam_zf9v034_port.hpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/drv_disp_ssd1306_port.hpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/drv_dmadvp_port.cpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/drv_dmadvp_port.hpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/drv_imu_port.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/drv_imu_port.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/hitsic_common.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/hitsic_common.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/inc_fsl_mk66f18.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/sys_extint_port.cpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/sys_extint_port.hpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/sys_pitmgr_port.cpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/sys_pitmgr_port.hpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/sys_uartmgr_port.cpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/d_mk66f18/sys_uartmgr_port.hpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/deprecated/drv_softi2c.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/deprecated/drv_softi2c.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/deprecated/drv_softi2c_port.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/deprecated/rte_i2c.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/deprecated/rte_i2c.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/deprecated/rte_spi.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/deprecated/rte_spi.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/deprecated/rte_uart.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/deprecated/rte_uart.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/CmBacktrace-1.4.0/cm_backtrace/cm_backtrace.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/CmBacktrace-1.4.0/cm_backtrace/cm_backtrace.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/inc/easyflash.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/plugins/types/struct2json/inc/cJSON.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/plugins/types/struct2json/inc/s2j.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/plugins/types/struct2json/inc/s2jdef.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/plugins/types/struct2json/src/cJSON.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/plugins/types/struct2json/src/s2j.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/plugins/types/ef_types.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/plugins/types/ef_types.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/src/easyflash.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/src/ef_env.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/src/ef_env_legacy.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/src/ef_env_legacy_wl.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/src/ef_iap.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/src/ef_log.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/extlib/EasyFlash-4.0.0/easyflash/src/ef_utils.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/app_menu.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/app_menu.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/app_menu_button.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/app_menu_button.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/app_menu_def.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/app_menu_nvm.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/app_menu_nvm.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/app_menu_type.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/app_menu_type.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_button.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_button.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_cam_zf9v034.cpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_cam_zf9v034.hpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_disp_font.cpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_disp_ssd1306.cpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_disp_ssd1306.hpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_disp_st7789.cpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_disp_st7789.hpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_dmadvp.cpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_dmadvp.hpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_ftfx_flash.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_ftfx_flash.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_imu_invensense.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/drv_imu_invensense.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/inc_stdlib.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/lib_adrcctrl.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/lib_adrcctrl.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/lib_list.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/lib_list.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/lib_pidctrl.c
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/lib_pidctrl.h
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/sys_extint.cpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/sys_extint.hpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/sys_pitmgr.cpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/sys_pitmgr.hpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/sys_rmcall.cpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/sys_rmcall.hpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/sys_uartmgr.cpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities/sys_uartmgr.hpp
        HITSIC_MK66F18_MCUX/HITSIC_Module/utilities_test/drv_cam_zf9v034_test.hpp
        HITSIC_MK66F18_MCUX/osa/usb_osa.h
        HITSIC_MK66F18_MCUX/osa/usb_osa_freertos.c
        HITSIC_MK66F18_MCUX/osa/usb_osa_freertos.h
        HITSIC_MK66F18_MCUX/sdmmc/host/fsl_sdmmc_host.c
        HITSIC_MK66F18_MCUX/sdmmc/host/fsl_sdmmc_host.h
        HITSIC_MK66F18_MCUX/sdmmc/inc/fsl_sd.h
        HITSIC_MK66F18_MCUX/sdmmc/inc/fsl_sdmmc_common.h
        HITSIC_MK66F18_MCUX/sdmmc/inc/fsl_sdmmc_spec.h
        HITSIC_MK66F18_MCUX/sdmmc/osa/fsl_sdmmc_osa.c
        HITSIC_MK66F18_MCUX/sdmmc/osa/fsl_sdmmc_osa.h
        HITSIC_MK66F18_MCUX/sdmmc/src/fsl_sd.c
        HITSIC_MK66F18_MCUX/sdmmc/src/fsl_sdmmc_common.c
        HITSIC_MK66F18_MCUX/source/ffconf.h
        HITSIC_MK66F18_MCUX/source/isr.cpp
        HITSIC_MK66F18_MCUX/source/main.cpp
        HITSIC_MK66F18_MCUX/source/syscalls.c
        HITSIC_MK66F18_MCUX/startup/startup_mk66f18.cpp
        HITSIC_MK66F18_MCUX/utilities/fsl_assert.c
        HITSIC_MK66F18_MCUX/utilities/fsl_debug_console.c
        HITSIC_MK66F18_MCUX/utilities/fsl_debug_console.h
        HITSIC_MK66F18_MCUX/utilities/fsl_debug_console_conf.h
        HITSIC_MK66F18_MCUX/utilities/fsl_shell.c
        HITSIC_MK66F18_MCUX/utilities/fsl_shell.h
        HITSIC_MK66F18_MCUX/utilities/fsl_str.c
        HITSIC_MK66F18_MCUX/utilities/fsl_str.h)
