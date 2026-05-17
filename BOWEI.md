npm run dev:server
CI=1 npm run web
socat TCP-LISTEN:6868,bind=172.22.17.9,reuseaddr,fork TCP:127.0.0.1:6767
vi ~/.paseo/config.json 

--- a~/.paseo/config.json
+++ b~/.paseo/config.json
@@ -3,7 +3,9 @@
   "daemon": {
     "listen": "127.0.0.1:6767",
     "cors": {
       "allowedOrigins": [
-        "https://app.paseo.sh"
+        "https://app.paseo.sh",
+        "http://localhost:8081",
+        "http://172.22.17.9:8081"
       ]
     },
