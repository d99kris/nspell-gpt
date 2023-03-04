# Project
cmake_minimum_required(VERSION 3.16 FATAL_ERROR)
project(nspell-gpt NONE)

# Program
configure_file(nspell-gpt ${CMAKE_CURRENT_BINARY_DIR}/nspell-gpt COPYONLY)
install(PROGRAMS nspell-gpt DESTINATION bin)

# Manuals
install(FILES nspell-gpt.1 DESTINATION share/man/man1)

# Uninstall
add_custom_target(uninstall
  COMMAND "${CMAKE_COMMAND}" -E remove "${CMAKE_INSTALL_PREFIX}/bin/nspell-gpt"
  COMMAND "${CMAKE_COMMAND}" -E remove "${CMAKE_INSTALL_PREFIX}/share/man/man1/nspell-gpt.1"
)
