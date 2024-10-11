上传图片到github上，生成链接在Typora中使用（解决Typora的md文件在分享时的丢失问题）

# 在GitHub上从操作

## **创建一个 GitHub 仓库：**

- 登录 GitHub，创建一个新的仓库来存储图片。
- ![](https://raw.githubusercontent.com/WANGmiaorui/-Typora_picture/%E4%B8%80%E4%BA%9B%E7%9E%8E%E6%8D%A3%E9%BC%93%E7%9A%84%E4%B8%9C%E8%A5%BF/github_Typora202410112019097.png)

## **生成 GitHub 令牌：**

- 在 GitHub 中，前往“Settings” > “Developer settings” > “Personal access tokens”。<img src="https://raw.githubusercontent.com/WANGmiaorui/-Typora_picture/%E4%B8%80%E4%BA%9B%E7%9E%8E%E6%8D%A3%E9%BC%93%E7%9A%84%E4%B8%9C%E8%A5%BF/github_Typora202410112021122.png" style="zoom: 67%;" />
- ![](https://raw.githubusercontent.com/WANGmiaorui/-Typora_picture/%E4%B8%80%E4%BA%9B%E7%9E%8E%E6%8D%A3%E9%BC%93%E7%9A%84%E4%B8%9C%E8%A5%BF/github_Typora202410112039393.png)
- 点击“Generate new token”，选择合适的权限（如“repo” 和“public_repo”），生成后保存令牌。
- ![](https://raw.githubusercontent.com/WANGmiaorui/-Typora_picture/%E4%B8%80%E4%BA%9B%E7%9E%8E%E6%8D%A3%E9%BC%93%E7%9A%84%E4%B8%9C%E8%A5%BF/github_Typora202410112041637.png)
- **填写令牌信息：**
  - **Note**：输入一个方便识别的名称。
  - **Expiration**：选择令牌的过期时间。
  - **Scopes**：选择适当的权限，一般情况下选择“repo”或“public_repo”即可。

# PicGo

## **安装PicGo**

- **安装 PicGo：**
  - 下载并安装 PicGo，确保软件可以正常运行。
- **打开 PicGo：**
  - 启动 PicGo 应用程序。
- **进入插件设置：**
  - 在左侧菜单中，点击“插件设置”。
- **安装 GitHub 图床插件：**
  - 在插件市场中搜索“GitHub”，找到“GitHub 图床”插件并安装。

## **配置 PicGo**

- 在 PicGo 中选择“插件设置”，启用“GitHub图床”插件。
- 配置 GitHub 图床：
- ![image-20241011204244955](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20241011204244955.png)
- ![image-20241011204454347](https://raw.githubusercontent.com/WANGmiaorui/-Typora_picture/%E4%B8%80%E4%BA%9B%E7%9E%8E%E6%8D%A3%E9%BC%93%E7%9A%84%E4%B8%9C%E8%A5%BF/github_Typoraimage-20241011204454347.png)
  - 设定仓库名：设置 `repo` 为 `用户名/仓库名`。
  - 设定分支名：设置 `branch` 为 `main` 或 `master`。
  - 设置Token：输入生成的 GitHub 令牌。
  - 设置 `path` 为存放图片的路径。
  - **存储路径（path）：**
    - 设定为您希望图片存储在仓库中的文件夹路径，例如 `images/`。如果不需要子文件夹，也可以留空。
  - **自定义域名：**
    - 如果您配置了 GitHub Pages 或有自定义域名，填写完整的网址，例如 `https://yourdomain.com/`。
    - 如果没有，可以留空，PicGo 会使用默认的 GitHub 文件链接。

**配置 Typora：**

![](https://raw.githubusercontent.com/WANGmiaorui/-Typora_picture/%E4%B8%80%E4%BA%9B%E7%9E%8E%E6%8D%A3%E9%BC%93%E7%9A%84%E4%B8%9C%E8%A5%BF/github_Typora202410112045450.png)

- 打开 Typora，进入“偏好设置”。
- 找到“图片”选项。
- 选择“上传服务”并选择“PicGo(app)”。

## **测试上传：**

![](https://raw.githubusercontent.com/WANGmiaorui/-Typora_picture/%E4%B8%80%E4%BA%9B%E7%9E%8E%E6%8D%A3%E9%BC%93%E7%9A%84%E4%B8%9C%E8%A5%BF/github_Typora202410112047132.png)

![](https://raw.githubusercontent.com/WANGmiaorui/-Typora_picture/%E4%B8%80%E4%BA%9B%E7%9E%8E%E6%8D%A3%E9%BC%93%E7%9A%84%E4%B8%9C%E8%A5%BF/github_Typora202410112047132.png)

- **打开 PicGo：**

  - 启动 PicGo 应用程序。

- **选择图片上传：**
  - 在主界面中，点击“上传图片”按钮。
  - 选择一张您希望测试上传的图片文件。

- **查看上传结果：**

  - 上传完成后，PicGo 会显示上传成功的提示。
  - 在提示中会提供图片的 URL 链接。

- **验证上传：**

  - 复制该 URL 链接，在浏览器中打开，查看图片是否可以正常显示。

- **检查 GitHub 仓库：**

  - 登录 GitHub，进入您的仓库。

  - 确认图片已上传到您指定的路径。

    

### PS

![image-20241011005926939](https://raw.githubusercontent.com/WANGmiaorui/-Typora_picture/%E4%B8%80%E4%BA%9B%E7%9E%8E%E6%8D%A3%E9%BC%93%E7%9A%84%E4%B8%9C%E8%A5%BF/github_Typoraimage-20241011005926939.png)

要把这个开开，才可以截屏后直接从剪切板传过去









