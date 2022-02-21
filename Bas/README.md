## bound와 frame 의 차이점을 설명하시오
<br>

    상위뷰 의지한다 ? → 바운드
    자기만의 아이덴티티가 있다 ?  → 프레임

- [블로그1](https://zeddios.tistory.com/203)
<br>

## 실제 디바이스가 없을 경우 개발 환경에서 할 수 있는 것과 없는 것을 설명하시오.
<br>

![이미지](https://user-images.githubusercontent.com/67938946/154877256-6b20ca74-dda6-4d74-87be-07e6c1af6eef.png)

- [공식문서](https://developer.apple.com/library/archive/documentation/IDEs/Conceptual/iOS_Simulator_Guide/TestingontheiOSSimulator/TestingontheiOSSimulator.html)
<br>

## 앱의 콘텐츠나 데이터 자체를 저장/보관하는 특별한 객체를 무엇이라고 하는가?
<br>
    
    Core Data

- [블로그](https://zeddios.tistory.com/987)
<br>

## 앱 화면의 콘텐츠를 표시하는 로직과 관리를 담당하는 객체를 무엇이라고 하는가?
<br>

    UIViewController

- [공식문서](https://developer.apple.com/library/archive/featuredarticles/ViewControllerPGforiPhoneOS/index.html#//apple_ref/doc/uid/TP40007457-CH2-SW1)
<br>

## App thinning에 대해서 설명하시오.
<br>

    애플리케이션이 디바이스에 설치될 때, 앱 스토어와 운영체제가 디바이스의 특성에 맞게 설치되도록 하는 설치 최적화 기술
    
- [블로그](https://zeddios.tistory.com/519)
- [블로그2](https://ttuk-ttak.tistory.com/42)
<br>

## 앱이 시작할 때 main.c 에 있는 UIApplicationMain 함수에 의해서 생성되는 객체는 무엇인가?
<br>

    UIApplication, Delegate

- [블로그](https://zeddios.tistory.com/539)
- [공식문서](https://developer.apple.com/documentation/uikit/1622933-uiapplicationmain)
<br>

## @Main에 대해서 설명하시오.
<br>

    앱은 프레임 워크의 기본 실행 시작점을 시작하기 위해 소량의 "부팅 로딩" 코드가 필요하다. 스위프트의 타입 기반의 시스템을 사용하여(@main) 간편한 진입점을 제공하여 문제를 해결한다.

- [블로그](https://barosalki.tistory.com/entry/iOS-Swift-53-main-type%EA%B8%B0%EB%B0%98%EC%9D%98-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%A8-%EC%A7%84%EC%9E%85%EC%A0%90)
<br>

## 앱이 foreground에 있을 때와 background에 있을 때 어떤 제약사항이 있나요?
<br>

    foreground
    저전력 모드에서 앱이 애니메이션 사용을 줄이고 프레임 속도를 낮추고 위치 업데이트를 중지하고 동기화 및 백업을 비활성화 하는 등의 작업을 할 수 있다.
    
    background
    1. 사용자의 이벤트를 못 받음
    2. 시간 제약이 있음
    3. 특정 유형의 앱만 돌릴 수 있음
    4. 메모리 제한도 있음(OS가 알아서 조정함)
    
- [블로그](https://icksw.tistory.com/178)
<br>

## 상태 변화에 따라 다른 동작을 처리하기 위한 앱델리게이트 메서드들을 설명하시오.
<br>

    //애플리케이션이 실행된 직후 사용자의 화면에 보여지기 직전에 호출 
    func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplicationLaunchOptionsKey: Any]?) -> Bool
    
    //애플리케이션이 최초 실행될 때 호출되는 메소드
    func application(_ application: UIApplication, willFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey : Any]? = nil) -> Bool

    //애플리케이션이 InActive 상태로 전환되기 직전에 호출  task 일시정지, 타이머 비활성화, 일시정지(게임)
    func applicationWillResignActive(_ application: UIApplication)    

    //애플리케이션이 백그라운드 상태로 전환된 직후 호출
    func applicationDidEnterBackground(_ application: UIApplication)    

    //애플리케이션이 Active 상태가 되기 직전, 화면에 보여지기 직전에 호출 
    func applicationWillEnterForeground(_ application: UIApplication)    

    //애플리케이션이 Active 상태로 전환된 직후 호출
    func applicationDidBecomeActive(_ application: UIApplication)

    //애플리케이션이 종료되기 직전에 호출 
    func applicationWillTerminate(_ application: UIApplication)    

- [블로그](https://medium.com/ios-development-with-swift/%EC%95%B1-%EC%83%9D%EB%AA%85%EC%A3%BC%EA%B8%B0-app-lifecycle-vs-%EB%B7%B0-%EC%83%9D%EB%AA%85%EC%A3%BC%EA%B8%B0-view-lifecycle-in-ios-336ae00d1855)
<br>

## 앱이 In-Active 상태가 되는 시나리오를 설명하시오.
<br>

    1. 사용자가 앱을 실행합니다.
    2. 앱 실행 도중 홈 버튼을 누릅니다.
    3. 앱을 다시 켭니다.
    4. 앱이 백그라운드에 있다가 Suspended 상태로 전이됩니다.

- [블로그](https://caution-dev.github.io/ios/2019/03/14/iOS-Application-state.html)
<br>

## scene delegate에 대해 설명하시오.
<br>

    화면에 표시되는 내용(Windows 또는 Scenes)을 처리하고 앱이 표시되는 방식을 관리

- [블로그](https://lena-chamna.netlify.app/post/appdelegate_and_scenedelegate/)
- [블로그2](https://zeddios.tistory.com/811)
<br>

## UIApplication 객체의 컨트롤러 역할은 어디에 구현해야 하는가?
<br>

    Application Delegate

- [블로그](https://daheenallwhite.github.io/ios/2019/07/18/UIApplication-UIWindow/)
<br>

## App의 Not running, Inactive, Active, Background, Suspended에 대해 설명하시오.
<br>

    1. Not Running : 앱이 아직 실행되지 않았거나, 완전히 종료되어 동작하지 않는 상태
    2. Inactive : app이 실행중이지만 사용자로부터 event를 받을 수 없는 상태
    3. Active : app이 실제 실행중이고 사용자 event를 받아서 상호작용할 수 있는 상태
    4. Background : 홈화면으로 나가거나 다른 app으로 전환되어 현재 app이 실질적인 동작을 하지 않는 상태
    5. Suspended : app을 다시 실행했을 때 최근 작업을 빠르게 로드하기 위해 메모리에 관련 데이터만 저장되어있는 상태

- [블로그](https://velog.io/@rnfxl92/%EC%95%B1-%EC%83%9D%EB%AA%85%EC%A3%BC%EA%B8%B0-Application-Life-Cycle)
<br>

## NSOperationQueue 와 GCD Queue 의 차이점을 설명하시오.
<br>

    1. NSOperationQueue 사용할 때 상당한 오버 헤드가 있다.
    2. NSOperationQueue 사용하면 GCD Queue보다 많은 코드를 필요로 해서 불편하다.
    3. NSOperationQueue 종속성에 대한 개념이 있다.
    
    - [스택오버플로우](https://stackoverflow.com/questions/10373331/nsoperation-vs-grand-central-dispatch)
<br>

## GCD API 동작 방식과 필요성에 대해 설명하시오.
<br>

    동작 방식 
    해야 할 일(코드)을 Operation으로 Wrapping한 다음에, Queue에 넣는다. Queue에서 남는 스레드에 작업을 배분한다.

    필요성 
    웹에서 이미지를 다운 받아서 사용자에게 보여준다고 했을 때, 비동기로 처리하지 않는다면 이미지를 다운받는 동안 다른 작업을 할 수 없기 때문에 앱이 멈춘다. 이렇게 비용이 많이 들어가는 작업을 메인 스레드에서 진행하면 사용자가 다른 작업을 할 수 없기 때문에 필요하다고 생각한다.
    
    - [깃허브](https://github.com/jwonyLee/TIL/blob/master/iOS/Interview/GCD-API.md)
<br>
