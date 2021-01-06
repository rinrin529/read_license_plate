# read_license_plate
 차량번호판 문자인식(OCR)

# 프로젝트 파이프라인
![image](https://user-images.githubusercontent.com/45943080/103255894-70d48a80-49ce-11eb-973a-179989419c62.png)


# Flow Chart
![image](https://user-images.githubusercontent.com/45943080/103255941-9feafc00-49ce-11eb-99a5-c6110bc1b269.png)


# 이미지 분할
이미지 분할이란 이미지에 존재하는 특정 객체를 인식하기 위해 전처리 과정을 하는 것이다. 
차량 번호판 이미지를 input 데이터로 설정하고, 이미지 분할을 진행한다.


![image](https://user-images.githubusercontent.com/45943080/103255967-c27d1500-49ce-11eb-9da6-58bcbc41bf83.png)


그림 2) 이미지 외곽 추출


그림2는 번호판 이미지의 외곽을 추출한 것이다. 
이미지 내부 존재하는 객체의 외곽을 추출하여 각각의 객체를 담은 contour box를 생성하도록 프로그램을 구현한다. 
가운데 7개의 box가 번호판 내부 문자를 나타내는 것이다. 이를 제외한 다른 것은 모두 불필요한 box이므로 제거하도록 해야 한다.


![image](https://user-images.githubusercontent.com/45943080/103256013-f35d4a00-49ce-11eb-81ac-b1d5a4979026.png)


그림 3) 이미지 분할 처리 완성


그림3은 불필요한 객체를 나타내는 box를 모두 제거하고 난 뒤의 모습이다. 
이미지 분할을 적용시킨 전처리 후의 이미지로 tesseract OCR를 사용하여 문자를 인식한 결과 인식률이 향상된 것을 알 수 있다. 

![image](https://user-images.githubusercontent.com/45943080/103256045-11c34580-49cf-11eb-8962-f42f65a6f8a4.png)


이미지 분할 적용 전

![image](https://user-images.githubusercontent.com/45943080/103256060-1ab41700-49cf-11eb-9295-8163a859d712.png)


이미지 분할 적용 후


그림 4) 이미지 이진화 적용
이미지 프로세싱의 최종 단계로 이미지 이진화를 통해 인식률을 향상시켰다.

![image](https://user-images.githubusercontent.com/45943080/103727323-59288200-501e-11eb-9ea3-924d3a511008.png)

