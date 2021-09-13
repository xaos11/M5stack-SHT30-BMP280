set(COMPONENT_SRCS "main.c")
# set(COMPONENT_ADD_INCLUDEDIRS "./includes")
set(COMPONENT_REQUIRES "nvs_flash" "esp-aws-iot" "esp-cryptoauthlib" "core2forAWS" "esp_idf_lib_helpers" "i2cdev" "bmp280" "sht3x" )
register_component()

target_add_binary_data(${COMPONENT_TARGET} "certs/aws-root-ca.pem" TEXT)
