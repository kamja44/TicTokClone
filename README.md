## SafeArea Widget

- 그 안에 있는 모든 것은 특정 공간에 있을 거라고 보장한다.
  - 공간은 확실하게 뭔가에 가려지지 않는다.

```dart
@override
  Widget build(BuildContext context) {
    return const Scaffold(
      body: SafeArea(
        child: Column(
          children: [
            Text("Sign up for TikTok"),
          ],
        ),
      ),
    );
  }
```

# 이벤트 감지

- eventListener
- GestureDetector

# 페이지 이동

Navigator

- 이벤트 감지 시 LoginScreen()으로 이동

sign_up_screen.dart

```dart
  void onLoginTap(BuildContext context) {
    Navigator.of(context).push(
      MaterialPageRoute(
        builder: (context) => const LoginScreen(),
      ),
    );
  }
```

## Navigator에 push가 아닌 pop을 하면 그 전 화면으로 이동한다.

- 즉, 유저가 보고 있는 현재 화면을 스택에서 제거한다.
  login_screen.dart

```dart
  void onLoginTap(BuildContext context) {
    Navigator.of(context).pop();
  }
```

# FractionallySizedBox

- 부모의 크기에 비례해서 크기를 정하게 해주는 Box 위젯
  - ex) 부모의 크기가 1000px이고, FractionallySizedBox의 widthFactor가 1이라면 FractionallySizedBox의 너비는 부모의 너비의 100%가 된다.
  - ex) 부모의 크기가 1000px이고, FractionallySizedBox의 widthFactor가 0.5이라면 FractionallySizedBox의 너비는 부모의 너비의 50%가 된다.

# fontAwsome 설치

`dependencies: font_awesome_flutter: 10.3.0`

# Expanded 위젯

- 사용할 수 있는 모든 공간을 사용한다.

```dart
Expanded(
              child: Text(
                text,
                style: const TextStyle(
                    fontSize: Sizes.size16, fontWeight: FontWeight.w800),
                textAlign: TextAlign.center,
              ),
            ),
```

# Stack 위젯

- 위젯들을 위에다가 쌓을 수 있게 한다.
  - 즉, 요소들이 서로 겹치는걸 허용한다.

## Stack의 Align 위젯

- stack에 있는 Widget 하나의 정렬만 바꿀 수 있게 해준다.

```dart
child: Stack(
          alignment: Alignment.center,
          children: [
             Align(
              alignment: Alignment.centerLeft,
              child: icon,
            ),
            Expanded(
              child: Text(
                text,
                style: const TextStyle(
                    fontSize: Sizes.size16, fontWeight: FontWeight.w800),
                textAlign: TextAlign.center,
              ),
            ),
          ],
        ),
```

# dart에서 메서드를 private으로 선언하는 방법

- 메서드의 이름 앞에 \_를 달아준다.
  - dart에는 public, private, protected와 같은 접근 제한자가 없기 때문이다.
