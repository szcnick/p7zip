

# WARNING : automatically generated by utils/generate.py
cmake_minimum_required(VERSION 2.8.12)

include_directories(
  "../../../myWindows"
  "../../../"
  "../../../include_windows"
)

add_definitions( -D_FILE_OFFSET_BITS=64 -D_LARGEFILE_SOURCE -D_REENTRANT -DENV_UNIX -DBREAK_HANDLER -DUNICODE -D_UNICODE -DUNIX_USE_WIN_FILE -DEXTRACT_ONLY -DNO_READ_FROM_CODER -D_SFX)

IF(APPLE)
  add_definitions(-DENV_MACOSX)
  FIND_LIBRARY(COREFOUNDATION_LIBRARY CoreFoundation )
ENDIF(APPLE)

add_executable(7zCon.sfx

  "../../../../C/7zCrc.c"
  "../../../../C/7zCrcOpt.c"
  "../../../../C/Aes.c"
  "../../../../C/Alloc.c"
  "../../../../C/Bcj2.c"
  "../../../../C/Bra.c"
  "../../../../C/Bra86.c"
  "../../../../C/BraIA64.c"
  "../../../../C/CpuArch.c"
  "../../../../C/Delta.c"
  "../../../../C/Lzma2Dec.c"
  "../../../../C/LzmaDec.c"
  "../../../../C/Ppmd7.c"
  "../../../../C/Ppmd7Dec.c"
  "../../../../C/Sha256.c"
  "../../../../C/Threads.c"
  "../../../../CPP/7zip/Archive/7z/7zDecode.cpp"
  "../../../../CPP/7zip/Archive/7z/7zExtract.cpp"
  "../../../../CPP/7zip/Archive/7z/7zHandler.cpp"
  "../../../../CPP/7zip/Archive/7z/7zHeader.cpp"
  "../../../../CPP/7zip/Archive/7z/7zIn.cpp"
  "../../../../CPP/7zip/Archive/7z/7zRegister.cpp"
  "../../../../CPP/7zip/Archive/Common/CoderMixer2.cpp"
  "../../../../CPP/7zip/Archive/Common/ItemNameUtils.cpp"
  "../../../../CPP/7zip/Archive/Common/OutStreamWithCRC.cpp"
  "../../../../CPP/7zip/Bundles/SFXCon/SfxCon.cpp"
  "../../../../CPP/7zip/Common/CWrappers.cpp"
  "../../../../CPP/7zip/Common/CreateCoder.cpp"
  "../../../../CPP/7zip/Common/FilePathAutoRename.cpp"
  "../../../../CPP/7zip/Common/FileStreams.cpp"
  "../../../../CPP/7zip/Common/FilterCoder.cpp"
  "../../../../CPP/7zip/Common/InBuffer.cpp"
  "../../../../CPP/7zip/Common/LimitedStreams.cpp"
  "../../../../CPP/7zip/Common/OutBuffer.cpp"
  "../../../../CPP/7zip/Common/ProgressUtils.cpp"
  "../../../../CPP/7zip/Common/StreamBinder.cpp"
  "../../../../CPP/7zip/Common/StreamObjects.cpp"
  "../../../../CPP/7zip/Common/StreamUtils.cpp"
  "../../../../CPP/7zip/Common/VirtThread.cpp"
  "../../../../CPP/7zip/Compress/Bcj2Coder.cpp"
  "../../../../CPP/7zip/Compress/Bcj2Register.cpp"
  "../../../../CPP/7zip/Compress/BcjCoder.cpp"
  "../../../../CPP/7zip/Compress/BcjRegister.cpp"
  "../../../../CPP/7zip/Compress/BranchMisc.cpp"
  "../../../../CPP/7zip/Compress/BranchRegister.cpp"
  "../../../../CPP/7zip/Compress/CopyCoder.cpp"
  "../../../../CPP/7zip/Compress/CopyRegister.cpp"
  "../../../../CPP/7zip/Compress/DeltaFilter.cpp"
  "../../../../CPP/7zip/Compress/Lzma2Decoder.cpp"
  "../../../../CPP/7zip/Compress/Lzma2Register.cpp"
  "../../../../CPP/7zip/Compress/LzmaDecoder.cpp"
  "../../../../CPP/7zip/Compress/LzmaRegister.cpp"
  "../../../../CPP/7zip/Compress/PpmdDecoder.cpp"
  "../../../../CPP/7zip/Compress/PpmdRegister.cpp"
  "../../../../CPP/7zip/Crypto/7zAes.cpp"
  "../../../../CPP/7zip/Crypto/7zAesRegister.cpp"
  "../../../../CPP/7zip/Crypto/MyAes.cpp"
  "../../../../CPP/7zip/UI/Common/ArchiveExtractCallback.cpp"
  "../../../../CPP/7zip/UI/Common/ArchiveOpenCallback.cpp"
  "../../../../CPP/7zip/UI/Common/DefaultName.cpp"
  "../../../../CPP/7zip/UI/Common/Extract.cpp"
  "../../../../CPP/7zip/UI/Common/ExtractingFilePath.cpp"
  "../../../../CPP/7zip/UI/Common/LoadCodecs.cpp"
  "../../../../CPP/7zip/UI/Common/OpenArchive.cpp"
  "../../../../CPP/7zip/UI/Common/PropIDUtils.cpp"
  "../../../../CPP/7zip/UI/Console/ConsoleClose.cpp"
  "../../../../CPP/7zip/UI/Console/ExtractCallbackConsole.cpp"
  "../../../../CPP/7zip/UI/Console/List.cpp"
  "../../../../CPP/7zip/UI/Console/MainAr.cpp"
  "../../../../CPP/7zip/UI/Console/OpenCallbackConsole.cpp"
  "../../../../CPP/7zip/UI/Console/PercentPrinter.cpp"
  "../../../../CPP/7zip/UI/Console/UserInputUtils.cpp"
  "../../../../CPP/Common/CRC.cpp"
  "../../../../CPP/Common/CommandLineParser.cpp"
  "../../../../CPP/Common/IntToString.cpp"
  "../../../../CPP/Common/MyString.cpp"
  "../../../../CPP/Common/MyVector.cpp"
  "../../../../CPP/Common/MyWindows.cpp"
  "../../../../CPP/Common/StdInStream.cpp"
  "../../../../CPP/Common/StdOutStream.cpp"
  "../../../../CPP/Common/StringConvert.cpp"
  "../../../../CPP/Common/UTFConvert.cpp"
  "../../../../CPP/Common/Wildcard.cpp"
  "../../../../CPP/Windows/ErrorMsg.cpp"
  "../../../../CPP/Windows/FileDir.cpp"
  "../../../../CPP/Windows/FileFind.cpp"
  "../../../../CPP/Windows/FileIO.cpp"
  "../../../../CPP/Windows/FileName.cpp"
  "../../../../CPP/Windows/PropVariant.cpp"
  "../../../../CPP/Windows/PropVariantConv.cpp"
  "../../../../CPP/Windows/Synchronization.cpp"
  "../../../../CPP/Windows/System.cpp"
  "../../../../CPP/myWindows/mySplitCommandLine.cpp"
  "../../../../CPP/myWindows/wine_date_and_time.cpp"
)


SET_TARGET_PROPERTIES(7zCon.sfx PROPERTIES SUFFIX "")

IF(APPLE)
   TARGET_LINK_LIBRARIES(7zCon.sfx ${COREFOUNDATION_LIBRARY} ${CMAKE_THREAD_LIBS_INIT})
ELSE(APPLE)
  IF(HAVE_PTHREADS)
   TARGET_LINK_LIBRARIES(7zCon.sfx ${CMAKE_THREAD_LIBS_INIT})
  ENDIF(HAVE_PTHREADS)
ENDIF(APPLE)

