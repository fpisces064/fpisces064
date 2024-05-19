import java.awt.*;
import java.awt.event.*;

public class GUIComponentsDemo {
    public static void main(String[] args) {
        Frame frame = new Frame("GUI Components Demo");
        
        Button button = new Button("Click Me!");
        Label label = new Label("Hello, GUI World!");
        TextField textField = new TextField("Type something here");
        Checkbox checkbox = new Checkbox("Check this");
        Choice choice = new Choice();
        choice.add("Option 1");
        choice.add("Option 2");
        choice.add("Option 3");
        List list = new List();
        list.add("Item 1");
        list.add("Item 2");
        list.add("Item 3");
        Canvas canvas = new Canvas();
        canvas.setSize(200, 200);
        
        frame.setLayout(new FlowLayout());
        frame.add(button);
        frame.add(label);
        frame.add(textField);
        frame.add(checkbox);
        frame.add(choice);
        frame.add(list);
        frame.add(canvas);
        
        frame.setSize(400, 300);
        frame.setVisible(true);

        button.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                label.setText("Button Clicked!");
            }
        });
        
        frame.addWindowListener(new WindowAdapter() {
            public void windowClosing(WindowEvent e) {
                System.exit(0);
            }
        });
    }
}

