# Raspberry_Project - RaspberryPi와 Arduino를 이용해 파테크 시작하기


* * *

# 🔍 목적
현대 사회에서는 물가 상승과 최저 시급의 증가로 인해 생활비 부담이 늘어나고 있습니다. 이에 따라 절약의 중요성이 더욱 부각되고 있습니다. 그중에서도 재테크뿐만 아니라 일상에서의 작은 절약도 큰 도움이 될 수 있습니다. 바쁜 현대인을 위해 라즈베리 파이를 활용하여 '파테크'를 통한 절약을 구현하려는 것이 이 프로젝트의 목적입니다.

# 🎯 목표
이 프로젝트는 라즈베리 파이와 아두이노를 활용하여 대파의 자동 관리 시스템을 구축하는 것을 목표로 합니다. 일정 시간마다 대파에 물을 주는 기능과 함께, 대파의 성장 과정을 라즈베리 파이의 카메라를 통해 사용자가 실시간으로 관찰할 수 있도록 하는 기능을 개발할 예정입니다. 이를 통해, 바쁜 일상 속에서도 대파를 효과적으로 관리하고, 그 결과로 생활비 절약에 도움을 주는 '파테크'를 실현하고자 합니다.

# 🛠️ 필요 재료
   1. 파이 카메라 : 대파의 성장을 일정 시간마다 카메라로 촬영 후 사용자에게 기록을 남겨주기 위해 필요.
   2. 아두이노 토양 수분 감지 센서 모듈 : 토양 내 수분함량에 따른 저항의 변화를 측정하는 센서로, 토양 내 수분함량에 따라 물의 공급 여부를 정하기 위해 필요.
   3. 아두이노(Uno) : 토양 수분 감지 센서의 아날로그 값과 워터 펌프를 통해 대파에 수분을 공급하는 명령을 위해 필요.
   4. 아두이노 워터 펌프(JT-180A) : 대파에 수분을 공급하기 위해 필요.
   5. 라즈베리파이 : 전체 시스템의 중앙 처리 장치로 사용하기 위해 필요.
   6. 조도 센서 : 화분 주변의 밝기를 측정하여 빛의 양을 측정하기 위해 필요.
   7. 식물 생장 LED : 부족한 광합성을 보충과 LED 작동을 위해 필요.
   8. 온습도 센서 : 온도와 습도를 측정해 사용자에게 텔레그램 메시지를 전달해주기 위해 필요.
   9. 화분 : 대파를 키우기 위한 공간 및 환경을 제공하기 위해 필요.

# 🌱 대파를 잘 키우기 위한 조건
   1. 토양: 대파는 비옥하고 잘 배수되는 토양을 선호합니다. 토양의 pH는 약 6.0~7.0이 이상적입니다.
   2. 물: 대파는 균일하게 물을 공급받아야 합니다. 토양이 마르지 않도록 주기적으로 물을 공급해야 합니다. 이는 토양 수분 센서를 사용하여 자동화할 수 있습니다.
   3. 온도: 대파는 선호하는 온도 범위가 있습니다. 일반적으로, 대파는 15~25도의 온도에서 가장 잘 자랍니다. (※5도 이하, 35도 이상일 경우 위험할 수 있음)
   4. 빛: 대파는 충분한 양의 햇빛을 필요로 합니다. 하루에 최소한 6시간 이상의 직사광선을 받아야 합니다. (※대파는 장일식물이기 때문에 24시간 직사광선에 노출되어도 좋음)
   5. 비료: 대파는 비료를 통한 영양분 공급이 필요합니다. 비료는 토양에 기본적인 영양소를 제공하며, 대파의 성장을 촉진합니다.

# 📷 참고 사진
# 파테크
![파테크](https://github.com/withoutsultang/Raspberry_Project/assets/113170868/eb217db7-61f5-48b9-b4b7-effccd96de1f)


출처: 구글 이미지
# 구현 이미지

![파테크_구현모습_수정본](https://github.com/withoutsultang/Raspberry_Project/assets/113170868/65f29a88-d3ff-4b38-8a1b-3bb6a6e0f8e2)

   
# 👨🏻‍💻 INHATC 3학년 2학기 무선네트워크 1조
<table>
  <tbody>
    <tr>
      <tr>
      <td align="center"><a href="https://github.com/withoutsultang"><img src="https://avatars.githubusercontent.com/u/120733105?v=4" width="100px;" alt=""/></td>
      <td align="center"><a href="https://github.com/youngsoosoo"><img src="https://avatars.githubusercontent.com/u/87405853?v=4" width="100px;" alt=""/></td>
      <td align="center"><a href="https://github.com/Kimsuji100"><img src="https://avatars.githubusercontent.com/u/113170868?v=4" width="100px;" alt=""/></td>
      <td align="center"><a href="https://github.com/dlrkd"><img src="https://avatars.githubusercontent.com/u/35716755?v=4" width="100px;" alt=""/></td>
      <td align="center"><a href="https://github.com/jys23"><img src="https://avatars.githubusercontent.com/u/113410132?v=4" width="100px;" alt=""/></td>
      </tr>
      <tr>
      <td align="center"><a href="https://github.com/withoutsultang">김건우</td>
      <td align="center"><a href="https://github.com/youngsoosoo">박용수</td>
      <td align="center"><a href="https://github.com/Kimsuji100">김수지</td>
      <td align="center"><a href="https://github.com/dlrkd">이강현</td>
      <td align="center"><a href="https://github.com/jys23">장용수</td>
      </tr>
    </tr>
  </tbody>
</table>
