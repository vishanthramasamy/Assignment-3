import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.ChoiceBox;
import javafx.scene.control.Label;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;

public class ColorChoiceBox extends Application {
    @Override
    public void start(Stage stage) {
        Label label = new Label("Select a color:");
        ChoiceBox<String> choiceBox = new ChoiceBox<>();

        choiceBox.getItems().addAll("Red", "Green", "Blue", "Yellow", "Purple");
        Label selectedColor = new Label("You selected: None");

        choiceBox.getSelectionModel().selectedItemProperty().addListener((v, oldValue, newValue) -> {
            selectedColor.setText("You selected: " + newValue);
        });

        VBox root = new VBox(10, label, choiceBox, selectedColor);
        Scene scene = new Scene(root, 300, 150);
        stage.setTitle("Color Selector");
        stage.setScene(scene);
        stage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
