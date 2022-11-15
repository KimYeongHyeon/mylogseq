- 문제해결
	- 날짜: 2022/11/15
	- 태그: GPU, CUDA, DBNet
	- 상태:
	- ## 발생상황
	- 분석계 workspace에서 EasyOCR사용간 dbNet 초기화시 컴파일 에러 발생
	- CPU는 이상없이 컴파일 완료
	- GPU 컴파일시 nvcc fatal: Unsupported gpu architecture 'compute_80' 이 뜨며 컴파일 실패
	- ## 이유
	- 1. cuda11.0이 compute_80을 지원
	  2. workspace의 GPU drive는 cuda 11 버전대이지만, CUDA compiler-drive tool인 nvcc는 10.2임
	- ## 해결방안
	-
	- ## 참고
	- 1. https://github.com/NVIDIA/cuda-samples/issues/44
	  2. https://stackoverflow.com/questions/53422407/different-cuda-versions-shown-by-nvcc-and-nvidia-smi