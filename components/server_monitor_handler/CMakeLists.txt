

idf_component_register(SRCS "server_monitor_handler.c"
                    INCLUDE_DIRS "."
					REQUIRES "esp_http_server" "spiffs")
					
# Create a SPIFFS image from the contents of the 'spiffs_image' directory
# that fits the partition named 'storage'. FLASH_IN_PROJECT indicates that
# the generated image should be flashed when the entire project is flashed to
# the target with 'idf.py flash'.
spiffs_create_partition_image(storage ./pages FLASH_IN_PROJECT)
				
