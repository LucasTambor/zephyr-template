# Set board
set(BOARD msp_exp432p401r_launchxl)

# Boilerplate code, which pulls in the Zephyr build system.
cmake_minimum_required(VERSION 3.13.1)
include($ENV{ZEPHYR_BASE}/cmake/app/boilerplate.cmake NO_POLICY_SCOPE)
project(my_zephyr_app)

# Add your source file to the "app" target. This must come after
# the boilerplate code, which defines the target.
target_sources(app PRIVATE src/main.c)


# If your application uses a configuration file or files other than the
# usual prj.conf add lines setting the CONF_FILE variable to these files appropriately.
# If multiple filenames are given, separate them by a single space or semicolon.
# CMake lists can be used to build up configuration fragment files in a modular way when you
# want to avoid setting CONF_FILE in a single place

#set(CONF_FILE "fragment_file1.conf")
#list(APPEND CONF_FILE "fragment_file2.conf")

# If your application uses a devicetree overlay file or files other than the usual <board>.overlay,
# add lines setting the DTC_OVERLAY_FILE variable to these files appropriately.

#set(DTC_OVERLAY_FILE "other_overlay.ovelay")
