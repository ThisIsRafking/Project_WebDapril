    String nama,kelas,nisn,mapel,Grade,Keterangan;
        
        double Harian,PAS,PTS,Rata2;
        nama = NAMA.getText();
        kelas = KELAS.getText();
        nisn = NISN.getText();
        mapel = MAPEL.getText();
        Harian = Double.parseDouble(N1.getText());
        PAS = Double.parseDouble(N2.getText());
        PTS = Double.parseDouble(N3.getText());
        Rata2 = (Harian + PAS + PTS) / 3.0;
        
        if (nama.isEmpty() || kelas.isEmpty() || nisn.isEmpty() || mapel.isEmpty()) {
        JOptionPane.showMessageDialog(null, "Maaf,FORM masih kosong");
        }
        
        if (Rata2 == 100) {
        Grade = "S";
        }
        
        else if (Rata2 >= 90) {
        Grade = "A";
        }
        
        else if (Rata2 <= 80) {
        Grade = "B";
        }
        
        else if (Rata2 >= 70) {
        Grade = "C";
        }
        else {
        Grade = "D";
        }
        
        if(Grade == "S") {
        Keterangan = "Kamu Lulus Dengan Nilai Terbaik Anjay";
        }
        
        else if(Grade == "A") {
        Keterangan = "Kamu Lulus Dengan Nilai Yang Bagus";
        }
        
        else if(Grade == "B" || Grade == "C") {
        Keterangan = "Kamu Dinyatakan Lulus";
        }
        
        else {
            Keterangan = "Kamu Tidak Lulus";
        }
        
        
        Tampil1.setText(nama);
        Tampil2.setText(nisn);
        Tampil3.setText(Double.toString(Rata2));
        Tampil4.setText(Grade);
        Tampil5.setText(Keterangan);
        Tampil6.setText(kelas);
