################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include emlib/subdir.mk
-include Drivers/subdir.mk
-include CMSIS/EFM32ZG/subdir.mk
-include BSP/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: STK3200_textdisplay_2.axf

# Tool invocations
STK3200_textdisplay_2.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: GNU ARM C Linker'
	arm-none-eabi-gcc -g -gdwarf-2 -mcpu=cortex-m0plus -mthumb -T "STK3200_textdisplay_2.ld" -Xlinker --gc-sections -Xlinker -Map="STK3200_textdisplay_2.map" --specs=nano.specs -o STK3200_textdisplay_2.axf "./BSP/bsp_bcc.o" "./BSP/bsp_stk.o" "./BSP/bsp_stk_leds.o" "./CMSIS/EFM32ZG/startup_efm32zg.o" "./CMSIS/EFM32ZG/system_efm32zg.o" "./Drivers/display.o" "./Drivers/displayls013b7dh03.o" "./Drivers/displaypalemlib.o" "./Drivers/i2cpsm.o" "./Drivers/retargetio.o" "./Drivers/retargettextdisplay.o" "./Drivers/rtcdriver.o" "./Drivers/si1147_i2c.o" "./Drivers/si114x_algorithm.o" "./Drivers/si114x_functions.o" "./Drivers/si7013.o" "./Drivers/textdisplay.o" "./Drivers/udelay.o" "./emlib/em_adc.o" "./emlib/em_assert.o" "./emlib/em_cmu.o" "./emlib/em_core.o" "./emlib/em_ebi.o" "./emlib/em_emu.o" "./emlib/em_gpio.o" "./emlib/em_i2c.o" "./emlib/em_leuart.o" "./emlib/em_prs.o" "./emlib/em_rtc.o" "./emlib/em_system.o" "./emlib/em_usart.o" "./src/main.o" -Wl,--start-group -lgcc -lc -lnosys -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

	@echo 'Building hex file: STK3200_textdisplay_2.hex'
	arm-none-eabi-objcopy -O ihex "STK3200_textdisplay_2.axf" "STK3200_textdisplay_2.hex"
	@echo ' '

	@echo 'Building bin file: STK3200_textdisplay_2.bin'
	arm-none-eabi-objcopy -O binary "STK3200_textdisplay_2.axf" "STK3200_textdisplay_2.bin"
	@echo ' '

	@echo 'Building s37 file: STK3200_textdisplay_2.s37'
	arm-none-eabi-objcopy -O srec "STK3200_textdisplay_2.axf" "STK3200_textdisplay_2.s37"
	@echo ' '

	@echo 'Running size tool'
	arm-none-eabi-size "STK3200_textdisplay_2.axf"
	@echo ' '

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) STK3200_textdisplay_2.axf
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
