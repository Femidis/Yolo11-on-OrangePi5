# Yolo11-on-OrangePi5

Необходим для конвертации нейронных сетей в формат rknn для выполнения на 
Rockchip NPU 
Для конвертации используются файлы из [rknn_model_ zoo](https://github.com/
airockchip/rknn_model_zoo/blob/main/examples/yolo11/python/).

Текущий релиз создан на rknn-toolkit2-2.3.2

1. Устанавливаем venv и pip

	```bash
	sudo apt-get install python3-venv
	sudo apt install python3-pip
	```

2. Создаём папку для виртуального окружения

	```bash
	скачать релиз
	распаковать
	cd ~/virtualenv
	```

3. Активируем виртуальное окружение
	
	```bash
	source bin/activate	
	```

4. Выполняем конвертацию

	Шаблон вызова сткрипта

	```bash
	python3 convert.py model_path [rk3566|rk3588|rk3562] [i8/fp] [output_path]
	```

	```bash
	python3 convert.py /path/to/cnn.onnx rk3588 i8 /path/to/result/cnn.rknn
	```

