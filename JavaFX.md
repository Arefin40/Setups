<h1 align="center">VS Code Setting for JavaFX</h1>

<p align="center">NOTE: You don't have to create any folder. A folder will be created automatically according to your project's name.</p>

## Setup

### Required Installation:

#### Extensions:

1. [Extension Pack for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack)
2. [SceneBuilder extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=bilalekrem.scenebuilderextension)

#### JavaFX SDK Setup

1. Download the [JavaFX SDK](https://download2.gluonhq.com/openjfx/21/openjfx-21_windows-x64_bin-sdk.zip) zip file.
2. Extract the zip file to your C drive JavaFX folder (<code>C:/JavaFX</code>) folder.

#### SceneBuilder Installation & Intregation

1. Download & install [SceneBuilder](https://download2.gluonhq.com/scenebuilder/21.0.0/install/win/SceneBuilder-21.0.0.msi).
2. Copy the SceneBuilder target path from properties.
3. Open VS Code Command Palette using <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>.
4. Type <code>configure scene builder path</code>.
5. Paste the previously copied SceneBuilder target path.

<br/>

## Create and Run JavaFX Project

<!-- ```JSONC
{
   "java.project.sourcePaths": ["src"],
   "java.project.outputPath": "bin",
   "java.project.referencedLibraries": [
      "lib/**/*.jar",
      "C:/JavaFX/javafx-sdk-21/lib/javafx-swt.jar",
      "C:/JavaFX/javafx-sdk-21/lib/javafx.base.jar",
      "C:/JavaFX/javafx-sdk-21/lib/javafx.controls.jar",
      "C:/JavaFX/javafx-sdk-21/lib/javafx.fxml.jar",
      "C:/JavaFX/javafx-sdk-21/lib/javafx.graphics.jar",
      "C:/JavaFX/javafx-sdk-21/lib/javafx.media.jar",
      "C:/JavaFX/javafx-sdk-21/lib/javafx.swing.jar",
      "C:/JavaFX/javafx-sdk-21/lib/javafx.web.jar"
   ]
}
``` -->

#### 👉🏻 Add <code>vmArgs</code> properties in your <code>.vscode/launch.json</code>

Update your JavaFX lib folder path

```JSON
"vmArgs" : "--module-path C:/JavaFX/javafx-sdk-21/lib --add-modules javafx.controls,javafx.fxml"
```

#### Example code for your main App

```Java
package application;

import javafx.application.Application;
import javafx.fxml.FXMLLoader;
import javafx.scene.Parent;
import javafx.scene.Scene;
import javafx.stage.Stage;

public class App extends Application {

   @Override
   public void start(Stage primaryStage) throws Exception {
      Parent root = FXMLLoader.load(getClass().getResource("yourFXML.fxml"));
      primaryStage.setTitle("MyApp");
      primaryStage.setScene(new Scene(root));
      primaryStage.show();
   }

   public static void main(String[] args) {
      launch(args);
   }
}
```
