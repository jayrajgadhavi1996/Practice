################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
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
all: led_D.axf

# Tool invocations
led_D.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"/home/jayraj/Documents/MCUXpresso_10.3.0_2200/workspace/lpc_board_nxp_lpcxpresso_1769/Debug" -L"/home/jayraj/Documents/MCUXpresso_10.3.0_2200/workspace/lpc_chip_175x_6x/Debug" -Xlinker -Map="led_D.map" -Xlinker --gc-sections -Xlinker -print-memory-usage -mcpu=cortex-m3 -mthumb -T "led_D_Debug.ld" -o "led_D.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) led_D.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "led_D.axf"; # arm-none-eabi-objcopy -v -O binary "led_D.axf" "led_D.bin" ; # checksum -p LPC1769 -d "led_D.bin";
	-@echo ' '

.PHONY: all clean dependents post-build

-include ../makefile.targets
