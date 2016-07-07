add_library(ming_curl Curl.cc)
target_link_libraries(ming_curl muduo_net)
target_link_libraries(ming_curl curl)

install(TARGETS ming_curl DESTINATION lib)
install(FILES Curl.h DESTINATION include/muduo/curl)

add_executable(mcurl mcurl.cc)
target_link_libraries(mcurl ming_curl)

add_executable(curl_download download.cc)
target_link_libraries(curl_download ming_curl)

