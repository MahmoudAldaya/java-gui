package com.example.game;

import javafx.application.Application;
import javafx.event.ActionEvent;
import javafx.event.EventHandler;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.control.Label;
import javafx.scene.layout.GridPane;
import javafx.stage.Stage;
import java.io.IOException;

public class HelloApplication extends Application {
    int p1c = 0;
    int p2c = 0;

    @Override
    public void start(Stage stage) throws IOException {
        Label p1 = new Label("Player 1");
        Label p2 = new Label("Player 2");

        Label p1result = new Label();
        Label p2result = new Label();

        Label result = new Label();

        Label p1score = new Label();
        Label p2score = new Label();

        Button play = new Button("Play");



        play.setOnAction(new EventHandler<ActionEvent>() {
            @Override
            public void handle(ActionEvent actionEvent) {
                int x = getRandom();
                int y = getRandom();

                p1result.setText(x + "");
                p2result.setText(y + "");

                if (x > y) {
                    result.setText("Player 1 Won!");
                    p1c++;
                } else if (y > x) {
                    result.setText("Player 2 Won!");
                    p2c++;
                } else
                    result.setText("Draw");

                p1score.setText(""+ p1c);
                p2score.setText(""+ p2c);
            }
        });

        GridPane grid = new GridPane();
        grid.addRow(0, p1, p1result, p1score);
        grid.addRow(1, p2, p2result, p2score);
        grid.addRow(2, play, result);

        grid.setVgap(20);
        grid.setHgap(40);

        grid.setStyle("-fx-padding: 30;" +
                "-fx-background-color: #6bb37f");

        Scene scene = new Scene(grid, 300, 200);

        stage.setScene(scene);
        stage.show();
    }

    int getRandom(){
        return (int)(1+ Math.random()*4);
    }


    public static void main(String[] args) {
        launch();
    }
}

/*
0.0 * 4 = 0.0 + 1 = 1.0 => 1
0.1 * 4 = 0.4 + 1 = 1.4 => 1
0.2 * 4 = 0.8 + 1 = 1.8 => 1
0.3 * 4 = 1.2 + 1 = 2.2 => 2
0.4 * 4 = 1.6 + 1 = 2.6 => 2
0.5 * 4 = 2.0 + 1 = 3.0 => 3
0.6 * 4 = 2.4 + 1 = 3.4 => 3
0.7 * 4 = 2.8 + 1 = 3.8 => 3
0.8 * 4 = 3.2 + 1 = 4.2 => 4
0.9 * 4 = 3.6 + 1 = 4.6 => 4
 */
