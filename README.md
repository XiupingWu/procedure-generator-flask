# 焊接参数生成器

## 项目简介
本项目是一个基于 Flask 的 API，用于生成焊接参数。它使用机器学习模型来预测焊接过程中的各项参数，如焊接角度、峰值电流、基值电流等。项目旨在为焊接工程师提供一个快速、准确的参数生成工具。

## 声明
此项目为后端系统，前端部署于 [XiupingWu/welding-procedure-generator](https://github.com/XiupingWu/welding-procedure-generator)。该系统适配于金鲁鼎焊接技术有限公司的自动焊机，训练数据由金鲁鼎焊接技术有限公司出品的自动焊机收集并所有。

## 技术栈
- **Flask**: 用于构建 Web API。
- **Flask-CORS**: 处理跨域请求。
- **scikit-learn**: 用于加载和运行机器学习模型。
- **joblib**: 用于加载预训练的模型文件。
- **numpy**: 用于数值计算。

## 安装步骤
1. 克隆本仓库到本地：
   ```bash
   git clone https://github.com/your-repo/procedure-generator-flask.git
   ```
2. 进入项目目录：
   ```bash
   cd procedure-generator-flask
   ```
3. 安装依赖：
   ```bash
   pip install -r requirements.txt
   ```

## 使用方法
1. 启动 Flask 服务器：
   ```bash
   python index.py
   ```
2. 使用 `POST` 请求访问 `/api/predict` 接口，传入焊接参数，获取预测结果。示例请求体：
   ```json
   {
       "厚度": 10,
       "坡口角度": 30,
       "钝边": 2,
       "间隙": 1,
       "直径": 50,
       "增透剂": "是",
       "材质": "不锈钢"
   }
   ```
3. 使用 `POST` 请求访问 `/api/upload` 接口，上传焊接参数。

## 贡献
欢迎提交 Issue 和 Pull Request 来改进本项目。

## 许可证
本项目采用 MIT 许可证。详情请参阅 [LICENSE](LICENSE) 文件。

---

# Welding Parameter Generator

## Project Overview
This project is a Flask-based API for generating welding parameters. It uses machine learning models to predict various parameters during the welding process, such as welding angle, peak current, base current, etc. The project aims to provide welding engineers with a fast and accurate parameter generation tool.

## Declaration
This project is the backend system, with the frontend deployed at [XiupingWu/welding-procedure-generator](https://github.com/XiupingWu/welding-procedure-generator). The system is adapted for the automatic welding machines of Jin Luding Welding Technology Co., Ltd., and the training data is collected and owned by the automatic welding machines produced by Jin Luding Welding Technology Co., Ltd.

## Tech Stack
- **Flask**: For building the web API.
- **Flask-CORS**: For handling cross-origin requests.
- **scikit-learn**: For loading and running machine learning models.
- **joblib**: For loading pre-trained model files.
- **numpy**: For numerical computations.

## Installation Steps
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/your-repo/procedure-generator-flask.git
   ```
2. Navigate to the project directory:
   ```bash
   cd procedure-generator-flask
   ```
3. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. Start the Flask server:
   ```bash
   python index.py
   ```
2. Use a `POST` request to the `/api/predict` endpoint, passing in the welding parameters to get the prediction results. Example request body:
   ```json
   {
       "厚度": 10,
       "坡口角度": 30,
       "钝边": 2,
       "间隙": 1,
       "直径": 50,
       "增透剂": "是",
       "材质": "不锈钢"
   }
   ```
3. Use a `POST` request to the `/api/upload` endpoint to upload welding parameters.

## Contributing
We welcome issues and pull requests to improve this project.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details. 