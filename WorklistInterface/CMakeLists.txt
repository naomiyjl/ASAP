PROJECT(WorklistInterface)

IF (WIN32)
	SET(CMAKE_CXX_FLAGS ${CMAKE_CXX_FLAGS}\ /std:c++latest)
ELSE()
	SET(CMAKE_CXX_STANDARD 17)
ENDIF()

SET(CMAKE_AUTOMOC ON)


add_compile_definitions(BOOST_ALL_DYN_LINK)

SET(GROUP_DATA
	Data/DataTable.h
	Data/DataTable.cpp
	Data/DirectoryDataAcquisition.h
	Data/DirectoryDataAcquisition.cpp
	Data/DjangoDataAcquisition.h
	Data/DjangoDataAcquisition.cpp
	Data/FilelistDataAcquisition.h
	Data/FilelistDataAcquisition.cpp
	Data/SourceLoading.h
	Data/SourceLoading.cpp
	Data/Worklist_CSV_Example.h
	Data/Worklist_CSV_Example.cpp
	Data/WorklistDataAcquisitionInterface.h
	Data/WorklistDataAcquisitionInterface.cpp
)

SET(GROUP_GUI
	GUI/CompositeChild.h
	GUI/CompositeWindow.h
	GUI/ExternalSourceDialog.h
	GUI/IconCreator.h
	GUI/WorklistWindow.h
	GUI/CompositeChild.cpp
	GUI/CompositeWindow.cpp
	GUI/ExternalSourceDialog.cpp
	GUI/IconCreator.cpp
	GUI/WorklistWindow.cpp
)

SET(GROUP_SERIALIZATION
	Serialization/INI.h
	Serialization/JSON.h
	Serialization/Misc.h
	Serialization/INI.cpp
	Serialization/JSON.cpp
	Serialization/Misc.cpp
)