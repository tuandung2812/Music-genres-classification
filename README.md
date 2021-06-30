
# Tóm tắt vấn đề: 
   Xây dựng một model để phân biệt 10 thể loai nhạc khác nhau: blues, classical, country,
   disco, hiphop, jazz, metal, pop, reggae and rock

# Dataset:
   Data train gốc : GTZAN dataset :https://www.kaggle.com/andradaolteanu/gtzan-dataset-music-genre-classification , gồm 1000 file âm thanh 30 giây, mỗi thể loại 100 file. Mỗi file lại được cắt nhỏ thành 9 subsamples nhỏ.
   &nbsp;
   
   Data train bổ sung : do nhóm tự thu thập, gồm khoảng 500 file âm thanh 30 giây từ YouTube ( mỗi thể loại 50 file). Cũng được xử lí giống như data gốc
   &nbsp;
   
   
   Data Test: 11 file âm thanh riêng được thu thập từ YouTube
    &nbsp;

   Input : file âm thanh dạng .wav
    &nbsp;

   Output: 1 trong 10 thể loại nhạc
   &nbsp;

  Feature được sử dụng:
  &nbsp;
  
     + NN và SVM : Mean và variance của 20 MFCC đầu tiên ( được giải thích rõ hơn trong report)
     + CNN : Mel Spectrogram của file âm thanh
  
  
# Các thuật toán sử dụng :
  + Convolutional Neural Network
  + Artificial Neural Network
  + Support Vector Machine

# Kết quả thực nghiệm:
&nbsp;
   Được tóm tắt trong Presentation, và nhận xét sâu hơn trong Report
 
 # Cấu trúc :
 &nbsp;
 Tất cả nằm trong directory sourcecode_dataset
  &nbsp;

    + CNN source code, NN source code, SVM source code : Source code của mỗi thuật toán tương ứng. 
      Trong mỗi directory, có source code của model khi train với tập dataset gốc và source code của model khi train với tập data được bổ sung
      VD : ML_Project_NN.ipynb là source code của model train tập dataset gốc, ML_Project_NN_Mixed.ipynb là source code của model train trên tập dataset được bổ sung
    + Models : directory lưu lại các model 
    + Preprocessing and data crawling: directory chứa phần code dùng để thu thập data và xử lý, extract feature từ data
    + csv file : chứa file csv ghi lại thông số MFCC. Được dùng cho SVM và NN ( data_train là tập data ban đầu, data_mixed là tập data đã được bổ sung, data_test là
      tập data test)
    + Mel Spectrogram : https://drive.google.com/drive/u/1/folders/1KUATQ1zWfYH0b31kbVx2xQW81kBbycUE
         mel_spec.tar.gz : tập data gốc
         mel_spec_mix.zip : tập data được bổ sung
         mel_spec_test.zip : tập data test
    + Presentation : phần thuyết trình của nhóm. Tóm tắt các thông tin, kết quả cơ bản của Project
    + Report : Bài report của nhóm, được viết cặn kẽ hơn




# Phần do em đảm nhiệm:
  + Thuật toán ANN
  + Thu thập dữ liệu
  + Phân tích kết quả thực nghiệm
