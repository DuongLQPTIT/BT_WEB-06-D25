# BT_WEB-06-D25
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lê Quang Dương - Trang giới thiệu cá nhân</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #f0f4f8;
            color: #1a252c;
            line-height: 1.6;
        }

        .bg-car-header {
            width: 100%;
            background: linear-gradient(rgba(15, 23, 42, 0.65), rgba(15, 23, 42, 0.65)), 
                        url('ảnh5.jpg') center/cover no-repeat;
            padding: 150px 0;
            box-shadow: 0 4px 15px rgba(0,0,0,0.15);
        }

        .header-content {
            width: 100%;
            padding-left: 40px; 
            padding-right: 20px;
            display: flex;
            align-items: center;
            justify-content: flex-start; 
            gap: 25px;
            text-align: left;
        }

        .header-avatar {
            width: 110px;
            height: 110px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid #ffffff;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
            flex-shrink: 0;
        }

        .header-text h1 {
            font-size: 26px;
            font-weight: 700;
            margin-bottom: 4px;
            color: #ffffff;
        }

        .header-text h3 {
            font-size: 14px;
            font-weight: 600;
            color: #f59e0b;
            margin-bottom: 10px;
        }

        .header-text p {
            font-size: 13.5px;
            color: #e2e8f0;
            max-width: 800px;
        }

   
        main {
            max-width: 1200px;
            margin: 30px auto;
            padding: 0 20px;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 25px;
            align-items: start;
        }

        .card {
            background: #ffffff;
            border-radius: 12px;
            padding: 24px 28px;
            margin-bottom: 25px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.03);
        }

        .card h2 {
            font-size: 18px;
            color: #1e4273;
            margin-bottom: 16px;
            font-weight: 700;
        }

        .card h4 {
            font-size: 14px;
            color: #1e4273;
            margin-bottom: 10px;
            font-weight: 700;
        }

        .info-list p {
            font-size: 14px;
            margin-bottom: 12px;
            color: #334155;
        }


        .grid-subcol {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }

        ul {
            list-style: none;
        }

        ul li {
            position: relative;
            padding-left: 18px;
            font-size: 13.5px;
            margin-bottom: 8px;
            color: #334155;
        }

        ul li::before {
            content: "›";
            position: absolute;
            left: 0;
            top: -2px;
            color: #e2a049;
            font-weight: bold;
            font-size: 16px;
        }

        ol {
            padding-left: 20px;
            font-size: 13.5px;
            color: #334155;
        }

        ol li {
            margin-bottom: 8px;
        }

        a {
            color: #1e4273;
            text-decoration: underline;
            font-weight: 600;
        }

        a:hover {
            color: #e2a049;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
        }

        .gallery-item {
            position: relative;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            aspect-ratio: 4/3;
            background-color: #f1f5f9;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.05);
        }

        .gallery-item .caption {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(transparent, rgba(0,0,0,0.7));
            color: #ffffff;
            font-size: 11px;
            padding: 15px 8px 6px;
            text-align: center;
        }

        .schedule-table {
            width: 100%;
            border-collapse: collapse;
            font-size: 12.5px;
            text-align: center;
        }

        .schedule-table th, 
        .schedule-table td {
            border: 1px solid #cbe0f5;
            padding: 8px 4px;
            vertical-align: middle;
        }

        .schedule-table th {
            background-color: #2b70b6;
            color: #ffffff;
            font-weight: 700;
            font-size: 13px;
        }

        .schedule-table td {
            color: #8fa0b3;
            background-color: #ffffff;
        }

        .schedule-table td.has-class {
            background-color: #bce0f8;
            color: #0f3763;
            font-weight: 700;
            line-height: 1.3;
        }

        .schedule-table td.has-class small {
            display: block;
            margin-top: 2px;
            font-weight: 600;
            color: #1b497a;
            font-size: 11px;
        }

        /* Form Liên hệ */
        form .form-group {
            margin-bottom: 14px;
        }

        form label {
            display: block;
            font-size: 13px;
            font-weight: 600;
            color: #475569;
            margin-bottom: 4px;
        }

        form input[type="text"],
        form input[type="email"],
        form select,
        form textarea {
            width: 100%;
            padding: 9px 12px;
            border: 1px solid #cbd5e1;
            border-radius: 6px;
            font-size: 13.5px;
            outline: none;
            background-color: #f8fafc;
        }

        form input:focus, form select:focus, form textarea:focus {
            border-color: #1e4273;
            background-color: #ffffff;
        }

        form button {
            background-color: #1e4273;
            color: #ffffff;
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            font-size: 13.5px;
            cursor: pointer;
            transition: background 0.2s;
            width: 100%;
        }

        form button:hover {
            background-color: #102a45;
        }

        footer {
            text-align: center;
            padding: 20px;
            font-size: 13px;
            color: #64748b;
        }
    </style>
</head>
<body>


    <header class="bg-car-header">
        <div class="header-content">
            <img class="header-avatar" src="ảnh6.jpg" alt="Lê Quang Dương">
            <div class="header-text">
                <h1>Lê Quang Dương</h1>
                <h3>Khoa Công Nghệ Thông Tin Định Hướng Ứng Dụng - Khoá D25</h3>
                <p>
                    Xin chào! Mình là <strong>Dương</strong>, hiện đang là sinh viên <b>năm hai.</b>
                    Mình có niềm đam mê đặc biệt với <b>thể thao</b> và các dòng <i><b>xe phân khối lớn (PKL) , siêu xe (super car)</b></i>.
                    Rất vui được kết nối và chia sẻ cùng mọi người!
                </p>
            </div>
        </div>
    </header>

   
    <main>
        
        <div class="left-column">
            
  
            <section class="card">
                <h2>1. Giới thiệu bản thân</h2>
                <div class="info-list">
                    <p>Họ và tên: <strong>Lê Quang Dương</strong></p>
                    <p>Quê quán: <b>Hải Dương</b></p>
                    <p>Định Hướng: <b>Business Analyst</b></p>
                    <p><span>Website yêu thích: </span><a href="https://www.tiktok.com" target="_blank">TikTok</a></p>
                </div>
                <p style="font-size: 13px; color: #64748b; margin-top: 10px;">
                    <b>Mình muốn học hiểu sâu nhiều loại ngôn ngữ khác nhau và trau dồi thêm nhiều kỹ năng mềm để phục vụ cho công việc sau này. Đặc biệt mình muốn tạo ra các sản phẩm mang tính sáng tạo và ứng dụng ngay khi còn là sinh viên trên giảng đường đại học!</b>
                </p>
            </section>

            <section class="card">
                <h2>2. Sở thích &amp; Kỹ năng</h2>
                <div class="grid-subcol">
                    <div>
                        <h4>Sở thích</h4>
                        <ul>
                            <li>Bóng Đá</li>
                            <li>Nghe nhạc</li>
                            <li>Chơi game</li>
                        </ul>
                    </div>
                    <div>
                        <h4>Kỹ năng hiện có</h4>
                        <ol>
                            <li>Thành thạo cơ bản <strong>Python</strong></li>
                            <li>Thành thạo cơ bản <strong>HTML</strong></li>
                            <li>Thành thạo cơ bản <strong>CSS</strong></li>
                            <li>Chứng chỉ <strong>TOEIC 550</strong></li>
                        </ol>
                    </div>
                </div>

                <div style="margin-top: 20px;">
                    <h4>Công nghệ muốn học thêm</h4>
                    <ul>
                        <li>MOS</li>
                        <li>Photoshop</li>
                        <li>Lập Trình Nhúng</li>
                    </ul>
                </div>
            </section>

            <section class="card">
                <h2>3. Bộ sưu tập ảnh của tôi</h2>
                <div class="gallery-grid">
                    <div class="gallery-item">
                        <img src="ảnh1.jpg" alt="Ducati Panigale V4 S">
                        <div class="caption">Ducati Panigale V4 S</div>
                    </div>
                    <div class="gallery-item">
                        <img src="ảnh2.jpg" alt="Mô hình BMW S1000RR">
                        <div class="caption">Mô hình BMW S1000RR</div>
                    </div>
                    <div class="gallery-item">
                        <img src="ảnh3.jpg" alt="BMW M4 & S1000RR Concept">
                        <div class="caption">BMW M4 & S1000RR Concept</div>
                    </div>
                    <div class="gallery-item">
                        <img src="ảnh4.jpg" alt="Bộ sưu tập Xe cảnh sát & PKL">
                        <div class="caption">Bộ sưu tập Xe cảnh sát & PKL</div>
                    </div>
                </div>
            </section>

        </div>


        <div class="right-column">
            <section class="card">
                <h2>4. Thời khóa biểu</h2>
                <table class="schedule-table">
                    <thead>
                        <tr>
                            <th style="width: 20%;">Giờ</th>
                            <th style="width: 16%;">Thứ 2</th>
                            <th style="width: 18%;">Thứ 3</th>
                            <th style="width: 12%;">Thứ 4</th>
                            <th style="width: 18%;">Thứ 5</th>
                            <th style="width: 16%;">Thứ 6</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>07:00 - 09:00</td>
                            <td>-</td>
                            <td class="has-class">Triết học<br><small>501_HQV</small></td>
                            <td>-</td>
                            <td>-</td>
                            <td>-</td>
                        </tr>
                        <tr>
                            <td>09:00 - 10:00</td>
                            <td>-</td>
                            <td class="has-class">Triết học<br><small>501_HQV</small></td>
                            <td>-</td>
                            <td>-</td>
                            <td>-</td>
                        </tr>
                        <tr>
                            <td>10:00 - 12:00</td>
                            <td class="has-class">Lập trình web<br><small>HT2_HQV</small></td>
                            <td>-</td>
                            <td>-</td>
                            <td class="has-class">Lập trình hướng đối tượng<br><small>HT2_HQV</small></td>
                            <td>-</td>
                        </tr>
                        <tr>
                            <td>13:00 - 15:00</td>
                            <td>-</td>
                            <td>-</td>
                            <td class="has-class">Lập trình hướng đối tượng<br><small>501_HQV</small></td>
                            <td>-</td>
                            <td>-</td>
                        </tr>
                    </tbody>
                </table>
            </section>
            <section class="card" id="lien-he">
                <h2>5. Biểu mẫu liên hệ</h2>
                <form action="#" method="post">
                    <div class="form-group">
                        <label for="fullname">Họ và tên:</label>
                        <input type="text" id="fullname" name="fullname" placeholder="Nhập họ và tên..." required>
                    </div>

                    <div class="form-group">
                        <label for="email">Email liên hệ:</label>
                        <input type="email" id="email" name="email" placeholder="abc@gmail.com" required>
                    </div>

                    <div class="form-group">
                        <label for="topic">Lựa chọn định hướng nghề nghiệp:</label>
                        <select id="topic" name="topic">
                            <option value="chon">-- Chọn định hướng nghề nghiệp --</option>
                            <option value="khoa hoc may tinh">Computer Science</option>
                            <option value="An toan thong tin">Cybersecurity</option>
                            <option value="Du lieu">Data Science</option>
                        </select>
                    </div>

                    <div class="form-group">
                        <label for="message">Nội dung:</label>
                        <textarea id="message" name="message" rows="3" placeholder="Nhập nội dung tại đây..."></textarea>
                    </div>

                    <button type="submit">Gửi Tin Nhắn</button>
                </form>
            </section>

        </div>

    </main>

    <footer>
        <p>© 2026 Lê Quang Dương.Sáng tạo theo cách bạn muốn @</p>
    </footer>

</body>
</html>
