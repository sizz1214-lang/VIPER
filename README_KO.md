# VIPER RSR·BTR 별도 한국어 패치 v1

이 폴더에는 완성 게임 파일을 제외한 두 개의 독립 패치가 있습니다.

- `VIPER_RSR_Korean_Patch_v1.zip`: 기존 Win9x VIPER 패처 방식의 단일 Windows PE32 패처. 원본 판별, 자동 백업, 적용, 재적용 판별, 복원을 지원합니다.
- `VIPER_BTR_Korean_xdelta_v1.zip`: 일본어 원본 HDI와 원본 `FONT.BMP`에서 최종 한국어 HDI와 `hangul.bmp`를 만드는 xdelta 두 개와 해시 검증 적용기입니다.

각 ZIP 안의 `README_KO.md`를 먼저 읽고, `SHA256SUMS.txt`로 압축 해제 파일을 확인하십시오.

RSR은 패처와 정적 readback 검증을 통과했고 Wine에서 런처·SGS 엔진 진입을 확인했지만, 구형 DirectDraw 캡처 문제 때문에 한국어 글리프 직접 시각 검증은 보류 상태입니다.

BTR은 최종 HDI·폰트·Anex86 조합에서 읽을 수 있는 한국어 대사 `자! 오늘도 벌자!!`가 확인된 빌드입니다. HDI 패치와 폰트 패치를 반드시 함께 적용하고 Anex86 Font에 결과 `hangul.bmp`를 지정해야 합니다.
