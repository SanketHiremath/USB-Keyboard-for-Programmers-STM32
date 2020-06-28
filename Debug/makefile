################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include USB_DEVICE/Target/subdir.mk
-include USB_DEVICE/App/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Core/Src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Class/HID/Src/subdir.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
custom_keyboard.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
custom_keyboard.list \

OBJCOPY_BIN += \
custom_keyboard.bin \


# All Target
all: custom_keyboard.elf secondary-outputs

# Tool invocations
custom_keyboard.elf: $(OBJS) $(USER_OBJS) C:\Users\shashikant\STM32CubeIDE\workspace_1.0.1\custom_keyboard\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "custom_keyboard.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\shashikant\STM32CubeIDE\workspace_1.0.1\custom_keyboard\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="custom_keyboard.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

custom_keyboard.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "custom_keyboard.list"
	@echo 'Finished building: $@'
	@echo ' '

custom_keyboard.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "custom_keyboard.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
