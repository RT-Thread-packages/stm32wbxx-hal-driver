from building import *
import os

cwd = GetCurrentDir()
path = [os.path.join(cwd, 'Inc')]
src_path = os.path.join(cwd, 'Src')

CPPDEFINES = ['USE_HAL_DRIVER']

src = [
os.path.join(src_path, 'stm32wbxx_hal.c'),
os.path.join(src_path, 'stm32wbxx_hal_comp.c'),
os.path.join(src_path, 'stm32wbxx_hal_cortex.c'),
os.path.join(src_path, 'stm32wbxx_hal_crc.c'),
os.path.join(src_path, 'stm32wbxx_hal_crc_ex.c'),
os.path.join(src_path, 'stm32wbxx_hal_cryp.c'),
os.path.join(src_path, 'stm32wbxx_hal_cryp_ex.c'),
os.path.join(src_path, 'stm32wbxx_hal_dma.c'),
os.path.join(src_path, 'stm32wbxx_hal_dma_ex.c'),
os.path.join(src_path, 'stm32wbxx_hal_exti.c'),
os.path.join(src_path, 'stm32wbxx_hal_pwr.c'),
os.path.join(src_path, 'stm32wbxx_hal_pwr_ex.c'),
os.path.join(src_path, 'stm32wbxx_hal_rcc.c'),
os.path.join(src_path, 'stm32wbxx_hal_rcc_ex.c'),
os.path.join(src_path, 'stm32wbxx_hal_rng.c'),
os.path.join(src_path, 'stm32wbxx_hal_gpio.c'),
os.path.join(src_path, 'stm32wbxx_hal_hsem.c'),
]

if GetDepend(['RT_USING_SERIAL']) or GetDepend(['RT_USING_NANO', 'RT_USING_CONSOLE']):
    src += [os.path.join(src_path, 'stm32wbxx_hal_uart.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_uart_ex.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_usart.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_usart_ex.c')]
    

if GetDepend(['RT_USING_I2C']):
    src += [os.path.join(src_path, 'stm32wbxx_hal_i2c.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_i2c_ex.c')]

if GetDepend(['RT_USING_SPI']):
    src += [os.path.join(src_path, 'stm32wbxx_hal_spi.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_spi_ex.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_qspi.c')]

if GetDepend(['RT_USING_USB']):
    src += [os.path.join(src_path, 'stm32wbxx_hal_hcd.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_pcd.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_pcd_ex.c')]
    src += [os.path.join(src_path, 'stm32wbxx_ll_usb.c')]
    
if GetDepend(['RT_USING_HWTIMER']) or GetDepend(['RT_USING_PWM']):
    src += [os.path.join(src_path, 'stm32wbxx_hal_lptim.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_tim.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_tim_ex.c')]

if GetDepend(['RT_USING_ADC']):
    src += [os.path.join(src_path, 'stm32wbxx_hal_adc.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_adc_ex.c')]

if GetDepend(['RT_USING_RTC']):
    src += [os.path.join(src_path, 'stm32wbxx_hal_rtc.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_rtc_ex.c')]

if GetDepend(['RT_USING_WDT']):
    src += [os.path.join(src_path, 'stm32wbxx_hal_iwdg.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_wwdg.c')]

if GetDepend(['RT_USING_AUDIO']):
    src += [os.path.join(src_path, 'stm32wbxx_hal_sai.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_sai_ex.c')]
 
if GetDepend(['RT_USING_PM']):
    src += [os.path.join(src_path, 'stm32wbxx_hal_lptim.c')]

if GetDepend(['BSP_USING_ON_CHIP_FLASH']):
    src += [os.path.join(src_path, 'stm32wbxx_hal_flash.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_flash_ex.c')]
    src += [os.path.join(src_path, 'stm32wbxx_hal_flash_ramfunc.c')]

group = DefineGroup('STM32WB-HAL', src, depend = ['PKG_USING_STM32WB_HAL_DRIVER'], CPPPATH = path, CPPDEFINES = CPPDEFINES)

Return('group')
