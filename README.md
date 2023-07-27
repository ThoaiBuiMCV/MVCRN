# BASE STRUCTURE FOR REACT NATIVE
- Phiên bản sử dụng: RN 0.72.3, React 18.2.0

## Yêu câu cấu hình:
- Yêu cầu cấu hình, môi trường cài đặt như trên trang chủ của nhà phát triển: 
https://reactnative.dev/docs/environment-setup?package-manager=yarn&guide=native

- [Node.js >= 12](https://nodejs.org) and npm (Recommended: Use [nvm](https://github.com/nvm-sh/nvm))
- [yarn > v1.20.0](https://yarnpkg.com/)
- [Watchman](https://facebook.github.io/watchman)
- [Xcode >= 12](https://developer.apple.com/xcode)
- [Cocoapods >= 1.10.1](https://cocoapods.org)
- [JDK >= 11](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
- [Android Studio and Android SDK](https://developer.android.com/studio)

## Một số scripts được thêm vào file package.json đễ hỗ trợ develop tốt hơn
- Build apk release và build adb bundle upload store
- Clean thư mục và xoá cache ios Xcode build
- Chuyển đổi port khi chạy ứng dụng
- Set path cho android build trên mac M1 hoặc M2 khi bị đứng

## Môi trường sử dụng:
- [apisauce](https://github.com/infinitered/apisauce) dùng như middleware cho xử lý HTTP/HTTPS request
- [react-native-config](https://github.com/luggit/react-native-config) để quản lý môi trường phát triển.
- [react-navigation](https://reactnavigation.org/) để quản lý các màn hình (di chuyển qua lại, truyền dữ liệu, hiệu ứng di chuyển, ...) của ứng dụng.
- [redux](https://redux.js.org/) && [redux-toolkit](https://redux-toolkit.js.org/) để quản lý State của ứng dụng.
- [jest](https://facebook.github.io/jest/) and [react-native-testing-library](https://callstack.github.io/react-native-testing-library/) for testing.
- [react-native-elements](https://reactnativeelements.com/) sử dụng cho các component cơ bản.
- [react-native-vector-icons](https://reactnativeelements.com/) sử dụng cho các icon gọn nhẹ.
- [lottie-react-native](https://www.npmjs.com/package/lottie-react-native) hỗ trợ các ảnh động dạng json (có thể bỏ qua nếu không cần thiết)

## Cấu trúc thư mục: 
- `src`: Thư mục chính chứa tất cả code bên trong ứng dụng gồm có:
 + `assets`: thư mục lưu trữ media, images, fonts, etc cho ứng dụng.
 + `components`: thư mục chứa cá component dùng chung cho ứng dụng, phụ thuộc từng dự án cụ thể sẽ bổ sung hoặc chỉnh sửa thêm cho phù hợp.
 + `constants`: Thư mục chứa các dữ liệu không thay đổi của ứng dụng.
 + `localization`: Thư mục chứa các tệp ngôn ngữ của ứng dụng.
 + `navigation`: Thư mục quản lý các cấu trúc screens của ứng dụng.
 + `redux`: cấu hình redux của ứng dụng (dự án nhỏ thì không cần áp dụng vào)
 + `screens`: chứa các màn hình của ứng dụng bao gồm:
   - `Screen`: Each screen should be stored inside its folder and inside it a file for its code and a separate one for the styles and tests.
      - `components`
      - `ScreenName.js`
 + `utils`: chứa các component tiện ích như các hiệu ứng loading, kết quả tìm kiếm (không có dữ liệu), tuỳ chỉnh các Text, Style hay sử dụng.
 + `theme`: Thư mục lưu trữ theme của ứng dụng (bỏ qua nếu không cần thiết).
 + `services`: Thư mục lưu trữ cấu hình xử lý API của dụng.
 + `App.js`: thành phần chính để khởi động app.

- `libraries`: thư mục chứa các thư viện bên thứ 3 nếu có.
