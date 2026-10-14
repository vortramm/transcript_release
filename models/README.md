# 화자 구분 모델

`wespeaker_emb_fp16.tflite` — 목소리 특징(256차원)을 뽑는 화자 임베딩 모델입니다.
실시간번역 앱의 "화자 구분"을 켜면 앱이 이 파일을 한 번 내려받아 휴대폰 안에서만 씁니다.

- 원본: WeSpeaker ResNet34 (VoxCeleb 학습), <https://github.com/wenet-e2e/wespeaker>
- TFLite 변환본: <https://huggingface.co/litert-community/Speaker-Diarization-LiteRT>
- 라이선스: CC BY 4.0 (모델 가중치) — 변경 없이 재배포합니다.
- SHA-256: `4853c284fdb3e39bd41f692d0bc3fd5068bf78782792d8ef02a3283c9d97554d`

# 받아쓰기 모델 (Parakeet 110M, int8)

`parakeet-110m/` — NVIDIA Parakeet TDT 110M 영어 음성 인식 모델을 sherpa-onnx 형식(int8)으로 바꾼 것입니다.
실시간번역 앱의 "받아쓰기: Parakeet 가벼움"을 고르면 앱이 한 번 내려받아 휴대폰 안에서만 씁니다.
jsDelivr(파일당 20MB) 로 받으려고 encoder 를 18MB 조각(`.part0`~`.part7`)으로 나눴고, 앱이 이어 붙인 뒤 SHA-256 을 확인합니다.

- 원본: <https://huggingface.co/nvidia/parakeet-tdt_ctc-110m> (CC BY 4.0)
- 변환본: k2-fsa/sherpa-onnx `sherpa-onnx-nemo-parakeet_tdt_transducer_110m-en-36000-int8` — 변경 없이 재배포
- encoder.int8.onnx SHA-256: `0f35509ddeb9b39002fb077d979a9fe74f06eb0bc4dd5c34f512f82e5111d657`

정확도 높은 쪽(Parakeet TDT 0.6B v2, 630MB)은 Hugging Face(csukuangfj/sherpa-onnx-nemo-parakeet-tdt-0.6b-v2-int8)의 고정 커밋에서 직접 받습니다.
