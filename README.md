# 실시간번역 업데이트 채널

앱 내 업데이트용 공개 저장소입니다. `latest.json`과 APK만 보관합니다. 앱 소스는 비공개 저장소에 있습니다.

## 큰 파일(모델·실행기)은 이 줄기에 두지 않습니다
jsDelivr 는 커밋마다 저장소 전체를 GitHub 에서 받아 가므로, 저장소가 커지면 GitHub 가 막습니다(429, 2026-10-14).
그래서 main 에는 APK 와 latest.json 만 두고, 모델·실행기는 **그 파일만 든 작은 커밋**(별도 브랜치 `assets-*`)이나
예전 고정 커밋에서 받습니다. 앱은 고정 커밋 주소 + SHA-256 으로 받으므로 브랜치를 지워도 안 됩니다(커밋이 사라지면 못 받음).
- 화자 모델: 커밋 d9a1324 `models/wespeaker_emb_fp16.tflite`
- Parakeet 가벼움 + sherpa-onnx 실행기: 커밋 c1ed2df `models/parakeet-110m/`, `native/sherpa-onnx-1.13.8/`
- 번역 실행기(llama.cpp): 브랜치 `assets-translate-62df1815`
