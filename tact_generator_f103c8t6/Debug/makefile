################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
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
tact_generator_f103c8t6.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
tact_generator_f103c8t6.list \

OBJCOPY_BIN += \
tact_generator_f103c8t6.bin \


# All Target
all: tact_generator_f103c8t6.elf secondary-outputs

# Tool invocations
tact_generator_f103c8t6.elf: $(OBJS) $(USER_OBJS) F:\CytomertGetDataSystem\Firmware_for_cytometr\tact_generator_f103c8t6\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "tact_generator_f103c8t6.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"F:\CytomertGetDataSystem\Firmware_for_cytometr\tact_generator_f103c8t6\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="tact_generator_f103c8t6.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

tact_generator_f103c8t6.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "tact_generator_f103c8t6.list"
	@echo 'Finished building: $@'
	@echo ' '

tact_generator_f103c8t6.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "tact_generator_f103c8t6.bin"
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
