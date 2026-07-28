add_llvm_library(LLVMObfuscation
  Utils.cpp
  ObfuscationPassManager.cpp
  ObfuscationOptions.cpp
  IndirectBranch.cpp
  IndirectCall.cpp
  IndirectGlobalVariable.cpp
  Flattening.cpp
  StringEncryption.cpp
  LegacyLowerSwitch.cpp
  ConstantIntEncryption.cpp
  ConstantFPEncryption.cpp
  MicrosoftRTTIEraser.cpp
  SplitBasicBlock.cpp

  ADDITIONAL_HEADER_DIRS
  ${LLVM_MAIN_INCLUDE_DIR}/llvm/Transforms/Obfuscation

  DEPENDS
  LLVMObfuscation
  intrinsics_gen
  LLVMLinker
  )
