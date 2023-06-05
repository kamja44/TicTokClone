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
