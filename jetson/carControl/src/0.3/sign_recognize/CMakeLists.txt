
cmake_minimum_required(VERSION 2.8)

project( signRecognizer )
find_package( OpenCV REQUIRED )

set( source_files
	signsRecognizer.h
	signsRecognizer.cpp
)

set( lib_name signsRecognizer)
add_library( ${lib_name} ${source_files} )
target_link_libraries( ${lib_name} ${OpenCV_LIBS} radon)


#set( test_exec_name test-stop-sign)
#add_executable( ${test_exec_name}  test_stop_sign_detection.cpp )

#target_link_libraries( ${test_exec_name} ${lib_name} ${OpenCV_LIBS})
