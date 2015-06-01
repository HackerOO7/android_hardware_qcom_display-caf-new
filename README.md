# android_hardware_qcom_display-caf-new
LNX.LA.3.5.2.1.2-02600-8x26.0 patched build on CM for prebuilt kernel

# notice
maybe need do this:

```
diff --git a/services/surfaceflinger/Android.mk b/services/surfaceflinger/Android.mk
index 0166b89..54c1eed 100644
--- a/services/surfaceflinger/Android.mk
+++ b/services/surfaceflinger/Android.mk
@@ -115,7 +115,7 @@ endif
     LOCAL_C_INCLUDES += $(call project-path-for,qcom-display)/$(PLATFORM)/libgralloc
     LOCAL_C_INCLUDES += $(call project-path-for,qcom-display)/$(PLATFORM)/libqdutils
 ifeq ($(TARGET_QCOM_DISPLAY_VARIANT),caf-new)
-    LOCAL_CFLAGS += -DQCOM_B_FAMILY
+#    LOCAL_CFLAGS += -DQCOM_B_FAMILY
 endif
     LOCAL_SHARED_LIBRARIES += libqdutils
     LOCAL_CFLAGS += -DQCOM_BSP
```

