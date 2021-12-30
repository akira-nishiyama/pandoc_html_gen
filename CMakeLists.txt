CMAKE_MINIMUM_REQUIRED(VERSION 3.12)
project(pandoc_html_generation NONE)

function( add_html_target TARGET_NAME SRC_FILE)

  add_custom_command(
    OUTPUT ${TARGET_NAME}.html
    COMMAND pandoc ${SRC_FILE} -o ${CMAKE_CURRENT_BINARY_DIR}/${TARGET_NAME}.html
    DEPENDS ${SRC_FILE}
    )
  add_custom_target( gen_${TARGET_NAME} ALL
    DEPENDS ${TARGET_NAME}.html
    )
  
endfunction()

add_html_target(test ${CMAKE_CURRENT_SOURCE_DIR}/test.md)


