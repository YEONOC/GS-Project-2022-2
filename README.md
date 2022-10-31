# GS-Project-2022-2

## 유니티 버전 : 2021.3.9f1
### GameSoftwareProject만 다운받으시면 됩니다!
## [SampleScene]
- 구성 
    - MainCamera
    - Directional Light
    - Plane
    - Plane(1)
    - Cube
    - Sphere
        - car 1203 black
1. 3D Object Shpere 추가하고 해당 Shpere에 Prefab 활용하여 다양한 모습(차, 비행기 등)으로 변경. Asset Store에서 Shpere에 반영할 Asset을 import 하고 import한 prefab을 Shpere에 적용. 
    - ### 사용한 Asset
        - HQ Racing Car Model No.1203 v1.0
            - car 1203 black

2. 변수로 Cube 오브젝트를 제어하는 것으로 Cube와 Plane(바닥)을 생성하고 Cube에 Rigidbody 컴포넌트를 추가 속성창에서 Rigidbody 컴포넌트의 Use Gravity는 체크하지 않고 Gravity는 false 로 설정. Cube 스크립트에서 Rigidbody 컴포넌트 선언하고 Rigidbody의 method를 활용하여 false로 초기화된 Gravity를 true로 변경. Cube는 Plane(바닥) 보다는 위쪽에 위치하도록 Y축 값으로 설정. 실행 버튼을 클릭하여 게임창에서 Cube가 중력을 받고 내려가서 Plane(바닥)에 떨어지는지 확인.
    - ### GameObject
        - Cube
            - Rigidbody
                - Mass : 2
                - Drag : 0
                - Angular drag : 0.05
                - Use Gravity : false
                - Is Kinematic : false
    - ### C# Scripts
        - CubeRigid.cs

## [ParticleScene]
- 구성 
    - MainCamera
    - Directional Light
    - FX_Fire
        - FX_Smoke
1. Particle System을 추가하고 속성값 5개 이상 변경하여 반영
    - ### 사용한 Asset
        - War FX v1.8.04
    - ### FX_Fire (Mat_FireFX 적용)
        - Shape


            <img src="https://user-images.githubusercontent.com/39399715/198955975-5ae81e1a-f5e4-4869-9eb0-4ce537da54f5.png" width="40%" height="30%">
        - Color over Lifetime

            <img src="https://user-images.githubusercontent.com/39399715/198926535-9c3d3e5c-d01f-43fa-9ece-87e0bd09f3ec.png" width="20%" height="30%">
        
        - Size over Lifetime

            <img src="https://user-images.githubusercontent.com/39399715/198926843-bb311240-ab46-4d8b-b0d7-8d329e2b238c.png" width="40%" height="30%">

        - Rotation over Lifetime

            <img src="https://user-images.githubusercontent.com/39399715/198926932-0d46fa9b-9e1c-48f7-b868-142544fc53d7.png" width="40%" height="30%">

        - Noise

            <img src="https://user-images.githubusercontent.com/39399715/198927143-c8e0b4c9-454a-49c2-b85e-9d0241170e9f.png" width="40%" height="30%">
    - ### FX_Smoke (Mat_SmokeFX 적용)
        - Shape

            <img src="https://user-images.githubusercontent.com/39399715/198928075-8c54156e-573b-4961-8cfd-c0fd1a97c081.png" width="40%" height="30%">
        - Color over Lifetime

            <img src="https://user-images.githubusercontent.com/39399715/198927906-4730f34d-d383-46e6-bf9b-476724257993.png" width="40%" height="30%">    

        - Size over Lifetime

            <img src="https://user-images.githubusercontent.com/39399715/198928207-6f108a23-53f5-4835-baab-1ebe638dda55.png" width="40%" height="30%">
        - Renderer

            <img src="https://user-images.githubusercontent.com/39399715/198927257-d6203eab-19c8-4d68-996b-359ef01f47c1.png" width="40%" height="30%">

        - Rotation over Lifetime

            <img src="https://user-images.githubusercontent.com/39399715/198926932-0d46fa9b-9e1c-48f7-b868-142544fc53d7.png" width="40%" height="30%">
        - Noise

            <img src="https://user-images.githubusercontent.com/39399715/198927735-cf150e3b-3757-471d-b66e-a26f6f83018a.png" width="40%" height="30%">

## [TerrianScene]
- 구성 
    - MainCamera
    - Directional Light
    - Terrian
    - WindZone
1. 3D Object로 Terrain을 추가하고 표면(Layer) Texture 변경, Brush로 산, 언덕 만들고 나무, 잔디, Wind zone 추가
    - ### 사용한 Asset
        - Standard Assets (for Unity 2018.4) v1.1.6 Environments
            - 표면 Texture 
                - GrassHillAlbedo
                - GrassRockyAlbedo
                - brush 속성
                    - builtin_brush_2
                    - Brush Size : 15
                    - Opacity : 12
            - 나무
                - Broadleaf_Desktop
                - Broadleaf_Mobile
                - brush 속성
                    - Brush Size : 40
                    - Opacity : 83
            - 잔디
                - GrassFrond01AlbedoAlpha
                - GrassFrond02AlbedoAlpha
                - brush 속성
                    - builtin_brush_3
                    - Brush Size : 15
                    - Opacity : 1
                    - Target Strength : 0.8125
    - ### WindZone
        - 속성
            - Mode : Directional
            - Main : 1
            - Turbulence : 1
            - Pulse Magnitude : 0.5
            - Pulse Frequency : 0.01
## [BackgroundScene]
- 구성 
    - MainCamera
    - Directional Light
    - Player
        - jet
    - Background
1. 스크롤되는 배경화면 만들기 (5점)
    - ### 사용한 Asset
        - Space Warrior Jet v1
            - jet
        - MK - Space Background Parallax Maker v2.1
            - Space Background 1
    - ### C# Scripts
        - Background.cs