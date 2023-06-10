cmake_minimum_required(VERSION 3.5)

set(srcs
    src/Firebase.cpp
    src/json/FirebaseJson.cpp
    src/json/extras/print/fb_json_print.c
    src/json/MB_JSON/MB_JSON.c
    src/rtdb/FB_RTDB.cpp
    src/rtdb/QueryFilter.cpp
    src/rtdb/QueueInfo.cpp
    src/rtdb/QueueManager.cpp
    src/rtdb/stream/FB_MP_Stream.cpp
    src/rtdb/stream/FB_Stream.cpp
    src/session/FB_Session.cpp
    src/signer/Signer.cpp
    src/wcs/esp32/FB_TCP_Client.cpp
    src/wcs/esp8266/FB_TCP_Client.cpp
)

set(includedirs
    src
)

idf_component_register(SRCS ${srcs}
                    INCLUDE_DIRS ${includedirs}
                    REQUIRES "arduino"
                    PRIV_REQUIRES esp_http_client esp-tls
                    )


project(Firebase-ESP32)
