
add_llvm_library(LLVMHSAILDesc
  BRIGDwarfStreamer.cpp

  HSAILAsmBackend.cpp
  HSAILELFObjectWriter.cpp
  HSAILMCCodeEmitter.cpp
  HSAILMCTargetDesc.cpp
  HSAILTargetStreamer.cpp
  HSAILMCAsmInfo.cpp
  RawVectorOstream.cpp
  )

# FIXME: How does this work for every other target? None of them need
# to specify this dependency.
target_link_libraries(LLVMHSAILDesc PRIVATE LLVMHSAILAsmPrinter)
