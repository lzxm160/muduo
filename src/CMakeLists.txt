

if(CURL_FOUND)
  add_subdirectory(curl)
else()
  add_subdirectory(curl EXCLUDE_FROM_ALL)
endif()
