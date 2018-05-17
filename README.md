
## 다운로드

build.gradle(Module: app)의 dependencies에 아래 항목을 입력해준다.

implementation 'com.blankj:utilcode:1.15.1'

Sync Now를 클릭하면 끝!



## 사용 방법

아래처럼 onCreate에서 초기화를 해준다.

@Override

protected void onCreate(Bundle savedInstanceState)

{

    super.onCreate(savedInstanceState);

    setContentView(R.layout.activity_main);


    myip = (EditText) findViewById(R.id.etMyIP);


    Utils.init(this); // <-- 초기화

}


각각의 자바 파일명을 이용해 필요한 기능을 구현하면 끝!


- ActivityUtils.java

  List<Activity> aa = ActivityUtils.getActivityList();
  
- AppUtils.java

  if(AppUtils.isAppForeground()) {} else {}
  
- CleanUtils.java

  CleanUtils.cleanInternalCache();
