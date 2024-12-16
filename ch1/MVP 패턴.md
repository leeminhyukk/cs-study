# MVP 패턴

MVP 패턴은 MVC 패턴으로부터 파생되었으며, MVC에서 **Controller**에 해당하는 부분이 **Presenter**로 교체된 패턴입니다.  
**뷰(View)**와 **프레젠터(Presenter)**는 **일대일 관계**를 가지므로, MVC 패턴보다 더 강한 결합을 지닌 디자인 패턴입니다.

---

## MVP 패턴의 구성

- **프레전터(Presenter) → 모델 변경 → 모델(Model)**
- **모델 → 모델 갱신 → 프레젠터(Presenter)**
- **프레젠터(Presenter) → UI 갱신 → View**
- **View → 유저 이벤트 → 프레젠터(Presenter)**

---

## MVP 패턴의 흐름

1. **View**에서 사용자 이벤트가 발생하면 **Presenter**로 전달됩니다.
2. **Presenter**는 이벤트를 처리하고 필요한 경우 **Model**의 데이터를 변경합니다.
3. **Model**은 데이터 갱신 상태를 **Presenter**에 알립니다.
4. **Presenter**는 갱신된 데이터를 기반으로 **View**를 업데이트합니다.

---

## 주요 특징
- **일대일 관계:** Presenter는 특정 View와 1:1로 연결됩니다.
- **분리된 역할:** View는 UI를 담당하며, Presenter는 로직을 처리합니다.
- **강한 결합:** Presenter와 View는 서로 긴밀히 연결되어 있습니다.
