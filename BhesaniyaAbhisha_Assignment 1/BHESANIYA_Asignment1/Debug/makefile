################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32L4xx_HAL_Driver/Src/subdir.mk
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
BHESANIYA_Asignment1.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
BHESANIYA_Asignment1.list \

OBJCOPY_BIN += \
BHESANIYA_Asignment1.bin \


# All Target
all: BHESANIYA_Asignment1.elf secondary-outputs

# Tool invocations
BHESANIYA_Asignment1.elf: $(OBJS) $(USER_OBJS) C:\ST\STM32CubeIDE_1.2.0\STM32CubeIDE\BHESANIYA_Asignment1\STM32L432KCUX_FLASH.ld
	arm-none-eabi-gcc -o "BHESANIYA_Asignment1.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\ST\STM32CubeIDE_1.2.0\STM32CubeIDE\BHESANIYA_Asignment1\STM32L432KCUX_FLASH.ld" --specs=nosys.specs -Wl,-Map="BHESANIYA_Asignment1.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

BHESANIYA_Asignment1.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "BHESANIYA_Asignment1.list"
	@echo 'Finished building: $@'
	@echo ' '

BHESANIYA_Asignment1.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "BHESANIYA_Asignment1.bin"
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
