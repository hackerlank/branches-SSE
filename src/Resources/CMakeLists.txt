ADD_LIBRARY(OpenEngine_Resources
  Resources.cpp
  IResource.h
  IModelResource.h
  IFontResource.h
  IFontTextureResource.h
  Types/ResourceTypes.h
  ITexture.h
  ITexture2D.h
  Texture2D.h
  ITexture3D.h
  Texture3D.h
  IShaderResource.h
  Exceptions.h
  File.h
  File.cpp
  Directory.h
  Directory.cpp
  ResourceManager.h
  DirectoryManager.h
  DirectoryManager.cpp
  IResourcePlugin.h
  IArchiveReader.h
  IArchiveReader.cpp
  IArchiveWriter.h
  IArchiveWriter.cpp
  StreamArchive.h
  StreamArchive.cpp
  BinaryStreamArchive.h
  BinaryStreamArchive.cpp
  SerializationResource.h
  SerializationResource.cpp
  IDataBlock.h
  DataBlock.h
  FrameBuffer.h
)

TARGET_LINK_LIBRARIES(OpenEngine_Resources
  OpenEngine_Utils
  
  OpenEngine_Scene
  # link to all libraries that have added serializable objects
  ${OE_SERIALIZABLE_OBJECT_EXTENSIONS}
)

IF(OE_BUILD_TESTS)
  SUBDIRS(tests)
ENDIF(OE_BUILD_TESTS)
