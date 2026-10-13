# 화자 구분 모델

`wespeaker_emb_fp16.tflite` — 목소리 특징(256차원)을 뽑는 화자 임베딩 모델입니다.
실시간번역 앱의 "화자 구분"을 켜면 앱이 이 파일을 한 번 내려받아 휴대폰 안에서만 씁니다.

- 원본: WeSpeaker ResNet34 (VoxCeleb 학습), <https://github.com/wenet-e2e/wespeaker>
- TFLite 변환본: <https://huggingface.co/litert-community/Speaker-Diarization-LiteRT>
- 라이선스: CC BY 4.0 (모델 가중치) — 변경 없이 재배포합니다.
- SHA-256: `4853c284fdb3e39bd41f692d0bc3fd5068bf78782792d8ef02a3283c9d97554d`
