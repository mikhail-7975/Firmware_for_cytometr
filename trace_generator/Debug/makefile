################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32H7xx_HAL_Driver/Src/subdir.mk
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
trace_generator.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
trace_generator.list \

OBJCOPY_BIN += \
trace_generator.bin \


# All Target
all: trace_generator.elf secondary-outputs

# Tool invocations
trace_generator.elf: $(OBJS) $(USER_OBJS) F:\CytomertGetDataSystem\Firmware_for_cytometr\trace_generator\STM32H743VITX_FLASH.ld
	arm-none-eabi-gcc -o "trace_generator.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m7 -T"F:\CytomertGetDataSystem\Firmware_for_cytometr\trace_generator\STM32H743VITX_FLASH.ld" --specs=nosys.specs -Wl,-Map="trace_generator.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv5-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

trace_generator.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "trace_generator.list"
	@echo 'Finished building: $@'
	@echo ' '

trace_generator.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "trace_generator.bin"
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
