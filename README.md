# Get Webtoon Image
If you want to use the webtoon data, run 'get_actual_toon_data.py'
## Prerequisites
It needs to download driver.exe.
If you use the chrome, you might use chromedriver.exe.
In this here, you can download chromedriver with your same chrome version.

'''
pip install selenium
pip install opencv-python
pip install natsort
'''

## Customization
### Episode: 
225번째, 227번째, 229번째 코드의 default값 수정
ex) 1화~100화 추출한다면 start는 100화, end는 1화
- 225번째 코드: default = ‘100화 링크’
- 227번째 코드: default = ‘1화 제목’
- 229번째 코드: default = 100
### Image size: 
아래와 같은 181번째 줄 코드에서 512가 이미지의 가로, 세로 크기(정사각형)

''' python
scale = cv2.resize(dst,(512,512),interpolation=cv2.INTER_LINEAR)
'''

## Run

'''
python get_actual_toon_data.py
'''

## Output Directory
- actual(원래 크기의 이미지)
- crop(지정한 크기에 맞춰 자른 이미지)

## File Name
EpisodeNumber_CutNumber.png
