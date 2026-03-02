<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ระบบรับซองของขวัญ - OSNVC</title>
    <style>
        :root {
            --yellow-alert: rgba(255, 193, 7, 0.2);
            --yellow-border: #ffc107;
            --flat-gray: #f4f4f4;
        }

        body { font-family: 'Kanit', sans-serif; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; background: #fafafa; }
        
        /* Container หลัก */
        .payment-card { width: 450px; padding: 20px; background: white; border-radius: 8px; box-shadow: 0 4px 10px rgba(0,0,0,0.05); }

        /* "ค่าเหลืองกรอกข้อมูลให้ครบ" Animation */
        .alert-yellow {
            display: none;
            background: var(--yellow-alert);
            border-left: 5px solid var(--yellow-border);
            padding: 10px;
            margin-bottom: 15px;
            border-radius: 4px;
            animation: pulse-yellow 2s infinite;
        }

        @keyframes pulse-yellow {
            0% { transform: scale(1); }
            50% { transform: scale(1.02); }
            100% { transform: scale(1); }
        }

        input { width: 100%; padding: 12px; margin: 8px 0; border: 1px solid #ddd; border-radius: 4px; box-sizing: border-box; }
        button { width: 100%; padding: 12px; background: #28a745; color: white; border: none; border-radius: 4px; cursor: pointer; font-weight: bold; }

        /* UI POP-UP Standard 450px */
        #popup-overlay {
            display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0,0,0,0.5); justify-content: center; align-items: center;
        }
        .popup-content {
            width: 450px; background: white; padding: 20px; border-radius: 0; /* แบน (Flat) */
            text-align: center; box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        }
        .popup-icon { font-size: 40px; margin-bottom: 10px; } /* ไอคอนห่างข้อความ 10px */
        .popup-msg { font-size: 18px; margin-bottom: 5px; }   /* ข้อความห่างปุ่ม 5px */
    </style>
</head>
<body>

<div class="payment-card">
    <h2 style="text-align:center;">เติมเงินผ่านซองของขวัญ</h2>
    
    <div id="yellow-warning" class="alert-yellow">
        ⚠️ กรุณากรอกข้อมูลให้ครบ
    </div>

    <input type="text" id="voucher_link" placeholder="วางลิงก์ซองของขวัญที่นี่...">
    <input type="text" id="mobile_no" placeholder="เบอร์โทรศัพท์รับเงิน" value="0812345678">
    <button onclick="submitPayment()">ยืนยันการรับเงิน</button>
</div>

<div id="popup-overlay">
    <div class="popup-content">
        <div id="pop-icon" class="popup-icon"></div>
        <div id="pop-text" class="popup-msg"></div>
        <button onclick="closePopup()">ตกลง</button>
    </div>
</div>

<script>
    const API_KEY = 'osnvc-key-188752442771';
    const API_URL = 'https://somo.osnvc.xyz/api/apiupth.php';

    async function submitPayment() {
        const link = document.getElementById('voucher_link').value;
        const mobile = document.getElementById('mobile_no').value;
        const yellowWarning = document.getElementById('yellow-warning');

        // ตรวจสอบข้อมูล (Validation)
        if (!link || !mobile) {
            yellowWarning.style.display = 'block';
            return;
        } else {
            yellowWarning.style.display = 'none';
        }

        try {
            // ส่งข้อมูลด้วย FormData ตามคำสั่ง cURL -d
            const formData = new FormData();
            formData.append('api_key', API_KEY);
            formData.append('link', link);
            formData.append('mobile', mobile);

            const response = await fetch(API_URL, {
                method: 'POST',
                body: formData
            });

            const result = await response.json();

            if (result.status === "success") {
                showPopup('✅', 'เติมเงินสำเร็จแล้ว!');
            } else {
                showPopup('❌', 'เกิดข้อผิดพลาด: ' + (result.message || 'ลิงก์ไม่ถูกต้อง'));
            }
        } catch (error) {
            showPopup('❌', 'ไม่สามารถเชื่อมต่อ API ได้');
        }
    }

    function showPopup(icon, text) {
        document.getElementById('pop-icon').innerText = icon;
        document.getElementById('pop-text').innerText = text;
        document.getElementById('popup-overlay').style.display = 'flex';
    }

    function closePopup() {
        document.getElementById('popup-overlay').style.display = 'none';
    }
</script>

</body>
</html>
