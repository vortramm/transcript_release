# 폰 안 번역 실행기 (llama.cpp 62df1815)

실시간번역 앱의 "기기 내 번역 고급(kanana)"이 번역 모델과 함께 받는 실행기입니다. APK 를 20MB 아래로 두려고 APK 에 넣지 않습니다.
llama.cpp(ggml-org/llama.cpp @ 62df1815bc053066761f4eac58e288f23778e164, MIT)를 정적으로 묶은 JNI 라이브러리를
CPU 세대별로 빌드했습니다(소스: 앱 저장소 `android/llm-native/`, `build-android.sh`).

- v8: 모든 arm64 / v82: armv8.2 + dotprod + fp16 / v86: armv8.6 + dotprod + i8mm + fp16
