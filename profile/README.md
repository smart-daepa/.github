# Raspberry_Project - <br> RaspberryPi와 Arduino를 이용해 파테크 시작하기


* * *

# 🔍 목적
현대 사회에서는 물가 상승과 최저 시급의 증가로 인해 생활비 부담이 늘어나고 있습니다. 이에 따라 절약의 중요성이 더욱 부각되고 있습니다. 그중에서도 재테크뿐만 아니라 일상에서의 작은 절약도 큰 도움이 될 수 있습니다. 바쁜 현대인을 위해 라즈베리 파이를 활용하여 '파테크'를 통한 절약을 구현하려는 것이 이 프로젝트의 목적입니다.

# 🎯 목표
이 프로젝트는 라즈베리 파이와 아두이노를 활용하여 대파의 자동 관리 시스템을 구축하는 것을 목표로 합니다. 일정 시간마다 대파에 물을 주는 기능과 함께, 대파의 성장 과정을 라즈베리 파이의 카메라를 통해 사용자가 실시간으로 관찰할 수 있도록 하는 기능을 개발할 예정입니다. 이를 통해, 바쁜 일상 속에서도 대파를 효과적으로 관리하고, 그 결과로 생활비 절약에 도움을 주는 '파테크'를 실현하고자 합니다.

# 🛠️ 필요 재료
<table style="width: 100%; border-collapse: collapse;">
  <tr style="background-color: lightgray;">
    <th style="border: 1px solid black; padding: 8px; text-align: center;">필요 재료</th>
    <th style="border: 1px solid black; padding: 8px; text-align: center;">제품명</th>
    <th style="border: 1px solid black; padding: 8px; text-align: center;">설명</th>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">파이 카메라</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">Pi Camera v2</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">대파의 성장을 일정 시간마다 카메라로 촬영 후 사용자에게 기록을 남겨주기 위해 필요.</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">아두이노 토양 수분 감지 센서 모듈</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">YL-69</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">토양 내 수분함량에 따른 저항의 변화를 측정하는 센서로, 물의 공급 여부를 판단하기 위해 필요. / 수분 함량이 높을수록 저항 값 ↓</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">아두이노</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">Uno</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">토양 수분 감지 센서 모듈의 아날로그 값과 워터 펌프를 통해 대파에 수분을 공급하는 명령을 위해 필요.</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">아두이노 워터 펌프</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">아두이노 워터펌프 모터 3~5V </td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">대파에 수분을 공급하기 위해 필요.</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">라즈베리 파이</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">3 B+</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">전체 시스템의 중앙 처리 장치로 사용하기 위해 필요.      </td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">조도 센서</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">Cds</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">빛의 양에 따라 전도율이 변하는 가변 저항 센서로, 화분 주변의 밝기를 측정하여 빛의 양을 측정하기 위해 필요. / 빛의 양이 적으면 저항 값 ↑</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">식물 생장 LED</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">-</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">부족한 광합성을 보충과 LED 작동을 위해 필요.</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">온습도 센서</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">DHT11</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;"> 온도와 습도를 측정해 사용자에게 텔레그램 메시지를 전달해주기 위해 필요. / 측정 습도 : 20 ~ 90%, 측정 온도 : 0 ~ 50℃</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">화분</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">-</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">대파를 키우기 위한 공간 및 환경을 제공하기 위해 필요.</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">토양</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">-</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">대파 뿌리를 심을 때 필요.</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">대파 뿌리</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">-</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">대파를 키우는 것이 목적이므로 필요.</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">물</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">-</td>
    <td style="border: 1px solid black; padding: 8px; text-align: center;">대파가 잘 자라려면 토양이 항상 적절히 촉촉하게 유지돼야 하므로 필요.</td>
  </tr>
</table>

# 확인 필요한 재료
   1. 온습도 센서
   2. 조도 센서
# 구매해야하는 것
   1. 아두이노 워터 펌프 : https://m.eduino.kr/product/detail.html?product_no=984
   2. 토양 수분감지 센서 모듈 : https://eduino.kr/product/detail.html?product_no=84&gad_source=1&gclid=Cj0KCQiAmNeqBhD4ARIsADsYfTf-WezOwrpHmkjXnWo13-KSgrxCWslWNDj-q-tiGj1VjCSWA2SA2-waAoSiEALw_wcB
   3. 흙 : 다이소
   4. 화분 : https://www.coupang.com/vp/products/72294667?itemId=241024909&vendorItemId=3593677979&q=화분&itemsCount=27&searchId=57ff756b726f43c19c86a9f26712ca19&rank=25&isAddedCart=
   5. 식물 생장 LED : https://robomall.co.kr/product/식물생장-led-조명-핀타입/23042/category/43/display/1/

# 🌱 대파를 잘 키우기 위한 조건
   1. 토양: 대파는 비옥하고 잘 배수되는 토양을 선호합니다. 토양의 pH는 약 6.0~7.0이 이상적입니다.
   2. 물: 대파는 균일하게 물을 공급받아야 합니다. 토양이 마르지 않도록 주기적으로 물을 공급해야 합니다. 이는 토양 수분 센서를 사용하여 자동화할 수 있습니다.
   3. 온도: 대파는 선호하는 온도 범위가 있습니다. 일반적으로, 대파는 15~25도의 온도에서 가장 잘 자랍니다. (※5도 이하, 35도 이상일 경우 위험할 수 있음)
   4. 빛: 대파는 충분한 양의 햇빛을 필요로 합니다. 하루에 최소한 6시간 이상의 직사광선을 받아야 합니다. (※대파는 장일식물이기 때문에 24시간 직사광선에 노출되어도 좋음)
   5. 비료: 대파는 비료를 통한 영양분 공급이 필요합니다. 비료는 토양에 기본적인 영양소를 제공하며, 대파의 성장을 촉진합니다.

# 🌲 (자동으로) 대파를 키우기 위한 준비 과정
   1. 화분에 준비한 흙(토양)을 담는다. 토양은 영양분이 많은 흙을 사용하거나 일반 흙에 계란 껍질 등을 활용하여 영양분이 풍부하게 한다.
   2. 마트에서 사온 파의 윗부분을 잘라서 뿌리만 화분에 심는다. 심을 때에는 파를 흙 깊숙히 집어 넣어야 파가 성장하면서 쓰러지지 않는다.
   3. 이렇게 심은 화분에 프로젝트 결과물을 설치한 후 화분을 햇빛이 잘드는 배란다나 창가 등에 옮겨둔다.
   4. 화분에 프로젝트 결과물을 설치할 때에는 토양감지센서가 흙에서 빠지지 않았는지, 조도센서가 장애물에 의해 가려지지 않았는지, 펌프가 연결된 물통에 물이 충분한지 등을 확인한다. 
   5. 토양에 물이 부족하면 토양습도감지계가 감지하여 화분에 물을 공급하여 화분이 마르지 않게 한다.
   6. 햇빛이 없는 밤시간에는 조도센서가 햇빛을 감지하여 화분에 설치한 식물 생장 LED를 켜주어 빛의 공급이 끊기지 않게 한다.
   7. 라즈베리 파이를 활용하여 파가 자라는 최적의 환경을 유지하며 파의 성장 사진을 받아가며 파가 잘 자라는지 확인한다.

# 📷 참고 사진
# 파테크
![파테크](https://github.com/withoutsultang/Raspberry_Project/assets/113170868/eb217db7-61f5-48b9-b4b7-effccd96de1f)


출처: 구글 이미지
# 구현 이미지

![파테크_구현모습_수정본](https://github.com/withoutsultang/Raspberry_Project/assets/113170868/65f29a88-d3ff-4b38-8a1b-3bb6a6e0f8e2)


# ⚙️ 시스템 흐름도

![smartdaepa_chart](https://github.com/smart-daepa/.github/assets/120733105/e9495e9a-9e76-400f-9cab-6e3276cb0c1e)

   
# 👨🏻‍💻 INHATC 3학년 2학기 무선네트워크 1조
<table>
  <tbody>
    <tr>
      <tr>
        <td align="center">토양 수분 감지 및<br>워터 펌프</td>
        <td align="center">온습도 센서<br>(텔레그램)</td>
        <td align="center">조도센서 빛의 양 확인<br>(LED)</td>
        <td align="center">파이카메라<br> 스케쥴링</td>
        <td align="center">데이터 베이스<br> 저장</td>
      </tr>
      <tr>
         <td align="center"><a href="https://github.com/withoutsultang"><img src="https://avatars.githubusercontent.com/u/120733105?v=4" width="100px;" alt=""/></td>
         <td align="center"><a href="https://github.com/youngsoosoo"><img src="https://avatars.githubusercontent.com/u/87405853?v=4" width="100px;" alt=""/></td>
         <td align="center"><a href="https://github.com/Kimsuji100"><img src="https://avatars.githubusercontent.com/u/113170868?v=4" width="100px;" alt=""/></td>
         <td align="center"><a href="https://github.com/dlrkd"><img src="https://avatars.githubusercontent.com/u/35716755?v=4" width="100px;" alt=""/></td>
         <td align="center"><a href="https://github.com/jys23"><img src="https://avatars.githubusercontent.com/u/113410132?v=4" width="100px;" alt=""/></td>
      </tr>
      <tr>
         <td align="center"><a href="https://github.com/withoutsultang">김건우<br>(withoutsultang)</td>
         <td align="center"><a href="https://github.com/youngsoosoo">박용수<br>(youngsoosoo)</td>
         <td align="center"><a href="https://github.com/Kimsuji100">김수지<br>(Kimsuji100)</td>
         <td align="center"><a href="https://github.com/dlrkd">이강현<br>(dlrkd)</td>
         <td align="center"><a href="https://github.com/jys23">장용수<br>(jys23)</td>
      </tr>
    </tr>
  </tbody>
</table>
