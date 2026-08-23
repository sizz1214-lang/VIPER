# VIPER RSR·BTR 별도 한국어 패치

완성 게임 파일을 제외한 독립 패치 모음입니다.

- `VIPER_RSR_Korean_Patch_v1.zip`: 기존 Win9x VIPER 패처 방식의 Windows 패처입니다. 원본 판별, 자동 백업, 적용, 재적용 판별, 복원을 지원합니다.
- `VIPER_BTR_Korean_xdelta_NotoRegular16_v2.zip`: 일본어 원본 HDI용 xdelta와 요청된 Noto Regular 16 기반 `font.bmp`를 함께 넣은 BTR 변형판입니다.
- `Viper_BTR_Korean_Final_v1.xdelta`와 `font.bmp`: BTR 수동 적용용 개별 파일입니다. 둘을 함께 사용해야 합니다.

기존 `VIPER_BTR_Korean_xdelta_v1.zip`은 이 Noto 폰트판으로 교체되어 현재 배포 목록에서 제거했습니다. 각 ZIP 안의 `README_KO.md`를 먼저 읽고 `SHA256SUMS.txt`로 압축 해제 파일을 확인하십시오.

## VIPER RSR 상태

패처와 정적 readback 검증을 통과했고 Wine에서 런처·SGS 엔진 진입을 확인했습니다. 구형 DirectDraw 캡처 문제 때문에 한국어 글리프 직접 시각 검증은 보류 상태입니다.

## VIPER BTR Noto Regular 16 상태

- 필요한 원본 `Viper BTR.hdi`: 20,786,176바이트, SHA-256 `dbc91f5d15eb7fb5400b6c82bc904223eb03f186280e8e7d94dede65cb755ef0`
- 패치 결과 HDI: SHA-256 `6c9fde1b237bf9dcb003b85a379264e2a4a53b2815aeb2809d9c458b3de0e479`
- 동봉 `font.bmp`: SHA-256 `73c354b307fce0098c9f49738199fd286cacb9352277c55a39648e0f5e2cd585`

HDI xdelta 디코드, ZIP 재해제, 폰트 2,350자 재생성 일치는 검증을 통과했습니다. 다만 이 정확한 Noto 폰트·HDI 조합은 Anex86 런타임 확인 전이므로 RC로 게시합니다. 기존 봉인 폰트가 포함된 별도 조합에서만 읽을 수 있는 한국어 대사 `자! 오늘도 벌자!!`가 실동작 확인됐습니다.

폰트의 Noto 유래 한글 글리프와 SIL Open Font License는 `FONT_PROVENANCE_AND_LICENSE.txt`를 확인하십시오.
