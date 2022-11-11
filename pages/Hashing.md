- hash: 다양한 크기의 입력에 대해 고정된 크기의 출력을 만드는 방법
-
- perceptual hashing algorithm 별 비교
- |algorithm|speed|accuracy|
  |ahash|fast|low|
  |phash|slow|high|
  |dhash|fast|high|
- https://fullstackml.com/wavelet-image-hash-in-python-3504fdd282b5
-
- #### 성능비교
- 출처: https://content-blockchain.org/research/testing-different-image-hash-functions/
- phash의 성능이 가장 낫다
-
- ## imagehash
- 주소: https://github.com/JohannesBuchner/imagehash
- 제공기능
	- * average hash
	  * 👁‍🗨 [[perceptual hash]] 
	  * difference hash
	  * wavelet hash
	  * HSV color hash (colorhash)
	  * Crop-resistant hash
-
-
- ## Using Lossy Hashing
- 출처: https://stackoverflow.com/questions/63195790/find-duplicate-images-in-fastest-way
- lossy hasing을 prefilter로 이용
- thumbnail를 생성해 similarity 계산 가능
-
- ## Raster data hash
- 출처: https://stackoverflow.com/questions/3383892/is-it-possible-to-detect-duplicate-image-files
- 코드1: https://packages.debian.org/stretch/python3-pythonmagick
- 다른 lossess compression과 다른 metadata를 갖고 있는 같은 이미지를 '같다'라고 하는데 도움을 줌
	- 우리 대부분의 데이터는 jpg, jpeg (lossy compression)인데 도움이 될까
-
- ## Dhash
- 출처: https://stackoverflow.com/questions/64625578/how-do-i-check-if-two-images-are-the-same-but-compressed-differently
- 코드1: https://github.com/benhoyt/dhash
- 코드2: https://github.com/Rayraegah/dhash; 테이블 참고바람
- 코드3: https://sangwook.github.io/2014/04/21/detecting-duplicate-images-using-python.html
- 간단한 알고리즘이라 비슷하거나 복사되었으나 잘려진 이미지에 대해선 작동이 잘 안할 수 있음
- 하지만 조광이 약간 다르다던가, 몇 픽셀이 잘려있다던가,가볍게 포토샵된 이미지에 대해선 잘 된다!
- 사용하기 위해 이미지를 간단하게 만들자
	- gray scale
	- Resize to 9x8
- |
-