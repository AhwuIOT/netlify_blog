### Reference
1. [中文官網-簡單的應用程式狀態管理](https://flutter.cn/docs/development/data-and-backend/state-mgmt/simple)
2. [第一個 state 管理 - Provider 的使用與深入](https://www.writershelf.com/article/%E7%AC%AC%E4%B8%80%E5%80%8B-state-%E7%AE%A1%E7%90%86-provider-%E7%9A%84%E4%BD%BF%E7%94%A8%E8%88%87%E6%B7%B1%E5%85%A5?locale=zh-TW&prne=roa)
3. [Day22 Flutter 的狀態管理 Provider (一)](https://ithelp.ithome.com.tw/articles/10250504)

---
### 實作
- [ChatGPT製作Todo-Provider](https://chat.openai.com/share/b3dd5006-141d-415a-a56a-ce2bde3a76ab)

---
### Provider概念
1. Provider是繼承自InheritedWidget
2. InheritedWidget目的是為了將資源傳下去
3. InheritedWidget在使用上有缺陷
4. InheritedWiget結合StatefulWidget與ChangeNotifier結合後成為Provider
5. Provider使用方式分為

> 1. Consumer
> 2. Provider.of(context)

