# Fabulously Optimized (mrpack to zip)

Kho lưu trữ các bản **Fabulously Optimized** đã được chuyển từ định dạng `.mrpack` sang `.zip`, sẵn sàng để giải nén và cài vào launcher Minecraft (Legacy Launcher, Fabric Launcher, Prism Launcher, v.v.).

> Repo này **không phải** là dự án chính thức của Fabulously Optimized. Toàn bộ công sức phát triển modpack thuộc về đội ngũ Fabulously Optimized và tác giả của từng mod bên trong. Xem phần [Bản quyền và ghi công](#bản-quyền-và-ghi-công).

---

## Mục lục

- [Fabulously Optimized là gì?](#fabulously-optimized-là-gì)
- [Tải file zip ở đâu?](#tải-file-zip-ở-đâu)
- [Yêu cầu trước khi cài](#yêu-cầu-trước-khi-cài)
- [Hướng dẫn cài nhanh](#hướng-dẫn-cài-nhanh)
- [Sửa lỗi thường gặp](#sửa-lỗi-thường-gặp)
- [Bản quyền và ghi công](#bản-quyền-và-ghi-công)

---

## Fabulously Optimized là gì?

**Fabulously Optimized** (viết tắt **FO**) là một modpack chạy trên nền **Fabric**, tập trung vào:

- Tăng FPS, giảm lag và giảm mức ngốn RAM của Minecraft.
- Giữ nguyên lối chơi vanilla, chỉ thêm các cải tiến nhỏ về hiệu năng, hình ảnh và giao diện.
- Phù hợp với **máy tính, laptop cấu hình thấp** muốn chơi Minecraft mượt hơn.

Modpack gốc được phát hành dưới dạng file `.mrpack` (định dạng của Modrinth). Một số launcher không đọc được `.mrpack` trực tiếp, vì vậy repo này cung cấp bản **đã chuyển sang `.zip`** để bạn chỉ cần giải nén và chép vào thư mục game.

Trang chính thức:

- Modrinth: <https://modrinth.com/modpack/fabulously-optimized>
- GitHub: <https://github.com/Fabulously-Optimized/fabulously-optimized>

---

## Tải file zip ở đâu?

Các file `.zip` được đăng ở mục **Releases** của repo, không nằm trong code.

1. Mở trang repo này trên GitHub.
2. Ở cột bên phải, bấm vào mục **Releases** (hoặc truy cập `https://github.com/<USER>/<REPO>/releases`).
3. Chọn bản phát hành mới nhất (nhãn **Latest**) hoặc bản khớp với phiên bản Minecraft bạn muốn chơi. Tên release thường có dạng `fabulously-optimized-<phiên bản>`.
4. Kéo xuống phần **Assets**, bấm vào file `mrpack-to-zip.zip` (hoặc file `.zip` có tên tương tự) để tải về.
5. Không tải mục `Source code (zip)` và `Source code (tar.gz)`, vì đó là mã nguồn của repo, không phải modpack.

> Thay `<USER>` và `<REPO>` bằng tên tài khoản và tên repo của bạn khi dán link vào bài viết.

---

## Yêu cầu trước khi cài

| Thành phần | Yêu cầu |
| --- | --- |
| Launcher | Legacy Launcher, Fabric Launcher, Prism Launcher hoặc launcher khác hỗ trợ Fabric |
| Minecraft | Đúng phiên bản mà bản release ghi rõ |
| Fabric | Đã tải sẵn phiên bản Minecraft có Fabric (mục `fabric-<version>` trong launcher) |
| Fabric API | **Bắt buộc** phải có, đúng phiên bản Minecraft |
| Java | Java 21 cho Minecraft 1.20.5 trở lên, Java 17 cho 1.18 đến 1.20.4 |
| RAM cấp cho game | Khuyến nghị 2GB đến 4GB |

Tải **Fabric API**:

- Modrinth: <https://modrinth.com/mod/fabric-api>
- CurseForge: <https://www.curseforge.com/minecraft/mc-mods/fabric-api>

> Phiên bản Minecraft, Fabric API và modpack phải **khớp nhau**. Lệch phiên bản sẽ làm game crash hoặc không mở được.

---

## Hướng dẫn cài nhanh

### Cách 1: Legacy Launcher và các launcher thường

1. **Tải phiên bản Minecraft có Fabric trước.** Mở launcher, chọn đúng phiên bản Minecraft, chọn loader Fabric, bấm Play để launcher tải về rồi thoát game. Khi thấy mục `fabric-<version>` trong danh sách là đã đúng.
2. **Mở thư mục game** (trong launcher bấm Open Game Folder, hoặc nhấn `Win + R`, gõ `%appdata%\.minecraft`).
3. **Giải nén** file zip vừa tải ra một thư mục tạm.
4. Nếu bên trong có thư mục `overrides`, mở vào trong nó. Chép các thư mục `mods`, `config`, `resourcepacks`, `shaderpacks` vào thư mục game, chọn **Replace** nếu máy hỏi ghi đè.
5. **Chép file Fabric API (`.jar`)** vào thư mục `mods`. Không giải nén file này.
6. Quay lại launcher, chọn mục `fabric-<version>` rồi bấm **Play**. Lần đầu mở sẽ lâu hơn bình thường.

> Thư mục `mods` phải nằm trực tiếp trong thư mục game, không phải kiểu `mods/mods/`.

### Cách 2: Prism Launcher

1. Bấm **Add Instance**, chọn tab **Import**.
2. Chọn file `.zip` vừa tải (hoặc file `.mrpack` gốc), bấm OK. Prism sẽ tự cài loader và mod.
3. Kiểm tra trong thư mục `mods` của instance đã có **Fabric API** chưa, nếu chưa thì thêm vào.

### Kiểm tra cài thành công

- Vào game, thấy mục **Mods** (nếu có) liệt kê Fabric API và các mod của modpack.
- Vào thế giới, nhấn `F3` để xem FPS, thường cao hơn rõ rệt so với vanilla.

---

## Sửa lỗi thường gặp

| Lỗi | Cách xử lý |
| --- | --- |
| Game crash ngay khi mở | Thiếu Fabric API hoặc sai phiên bản Minecraft |
| Không thấy mục `fabric-<version>` | Chưa tải phiên bản Minecraft có Fabric, hãy vào game vanilla Fabric một lần |
| Báo lỗi Java | Cài đúng Java 17 hoặc Java 21 rồi chọn lại Java Path trong launcher |
| Game vẫn giật | Giảm Render Distance xuống 6 đến 8 chunk, kiểm tra lại RAM cấp cho game |
| Báo mod xung đột | Xóa hết file trong `mods`, chép lại từ đầu và nhớ giữ Fabric API |

Nếu vẫn lỗi, hãy mở một [Issue](../../issues) kèm phiên bản Minecraft, tên launcher và file log (`latest.log`).

---

## Bản quyền và ghi công

- Modpack **Fabulously Optimized** và toàn bộ mod bên trong thuộc quyền của tác giả tương ứng, mỗi mod có giấy phép riêng. Vui lòng xem trang chính thức để biết chi tiết.
- Repo này chỉ lưu trữ bản chuyển định dạng để thuận tiện cài đặt, không chỉnh sửa nội dung mod.
- Nội dung do chủ repo tự viết (README, hướng dẫn) được phát hành theo giấy phép **MIT**, xem file [LICENSE](LICENSE).
- Minecraft là thương hiệu của Mojang Studios và Microsoft. Repo này không liên kết với Mojang hay Microsoft.

Nếu bạn là tác giả của modpack hoặc mod và muốn gỡ file khỏi repo, hãy mở Issue hoặc liên hệ chủ repo để được xử lý nhanh chóng.
