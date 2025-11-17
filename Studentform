import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.*;
import javafx.scene.layout.*;
import javafx.stage.Stage;

public class StudentForm extends Application {
    @Override
    public void start(Stage stage) {
        // Create input controls
        TextField nameField = new TextField();
        nameField.setPromptText("Enter Name");

        ToggleGroup genderGroup = new ToggleGroup();
        RadioButton male = new RadioButton("Male");
        RadioButton female = new RadioButton("Female");
        male.setToggleGroup(genderGroup);
        female.setToggleGroup(genderGroup);

        ComboBox<String> deptBox = new ComboBox<>();
        deptBox.getItems().addAll("IT", "CSE", "ECE", "EEE", "MECH");

        Button submitBtn = new Button("Submit");
        TextArea outputArea = new TextArea();

        submitBtn.setOnAction(e -> {
            String name = nameField.getText();
            RadioButton selectedGender = (RadioButton) genderGroup.getSelectedToggle();
            String gender = selectedGender != null ? selectedGender.getText() : "Not Selected";
            String dept = deptBox.getValue() != null ? deptBox.getValue() : "Not Selected";

            outputArea.setText("Student Details:\nName: " + name +
                               "\nGender: " + gender +
                               "\nDepartment: " + dept);
        });

        VBox root = new VBox(10,
                new Label("Name:"), nameField,
                new Label("Gender:"), new HBox(10, male, female),
                new Label("Department:"), deptBox,
                submitBtn, outputArea);

        Scene scene = new Scene(root, 400, 350);
        stage.setTitle("Student Information Form");
        stage.setScene(scene);
        stage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
