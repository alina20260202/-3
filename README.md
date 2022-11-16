# -3
страница 125 номер 18

Создать объект класса Пианино, используя классы Клавиша, Педаль. Методы: настроить, играть на пианино, нажимать клавишу

packagecom.company;
 
import javax.swing.*;

import java.awt.*;

import java.awt.event.KeyAdapter;

import java.awt.event.KeyEvent;

importjava.io.IOException;

 
public class Interf extends JFrame  {

    private JButton create;
    
    private JButton play;
    
    private JButtonperedati;
    
    private JButtonpriem;
    
    private JButton stop;
 
    public JRadioButton r1,r2,r3;
    
    public ButtonGroupbg = new ButtonGroup();
 
    Interf()
    
    {
        super("Пианино");
        
        setDefaultCloseOperation(EXIT_ON_CLOSE);
        
        setSize(570, 570);
 
        r1 = new JRadioButton("1");
        
        r1.setBounds(400,10,50,20);
        
        r2 = new JRadioButton("1/2");
        
        r2.setBounds(400, 30, 50, 20);
        
        r3 = new JRadioButton("1/4");
        
        r3.setBounds(400, 50, 50, 20);
        
        //обавляем в группу
        
        bg.add(r1);
        
        bg.add(r2);
        
        bg.add(r3);
        
        //указываемобработчик
        
        r1.setSelected(true);
        
       create = new JButton("Создан");

 
        create.setBounds(10, 450, 100, 30);
        
        play = new JButton("Воспроизведение");
        
        play.setBounds(120, 450, 100, 30);
        
        peredati = new JButton("Передача");
        
        peredati.setBounds(230, 450, 100, 30);
        
        priem = new JButton("Прием");
        
        priem.setBounds(340, 450, 100, 30);
        
        stop = new JButton("Стоп");
        
        stop.setBounds(450, 450, 100, 30);
        
 
        final JPanel piano = new JPanel();
        
        piano.setLayout(null);
        
        final JLabel keybut1 = new JLabel(new ImageIcon("key3.gif"));
        
        keybut1.setBounds(13, 0, 34, 288);
        
        final JLabel blackey1 = new JLabel(new ImageIcon("key4.gif"));
        
        blackey1.setBounds(35, 0, 28, 149);
        
        final JLabel keybut2 = new JLabel(new ImageIcon("key2.gif"));
        
        keybut2.setBounds(51, 0, 34, 288);
        
        final JLabel keybut3 = new JLabel(new ImageIcon("key1.gif"));
        
        keybut3.setBounds(99, 0, 34, 288);
        
        final JLabel keybut4 = new JLabel(new ImageIcon("key1.gif"));
        
        keybut4.setBounds(134, 0, 34, 288);
        
        final JLabel keybut5 = new JLabel(new ImageIcon("key1.gif"));
        
        keybut5.setBounds(169, 0, 34, 288);
        
        final JLabel keybut6 = new JLabel(new ImageIcon("key1.gif"));
        
        keybut6.setBounds(203, 0, 34, 288);
        
        final JLabel keybut7 = new JLabel(new ImageIcon("key1.gif"));
        
        keybut7.setBounds(238, 0, 34, 288);
        
        final JLabel keybut8 = new JLabel(new ImageIcon("key1.gif"));
        
        keybut8.setBounds(273, 0, 34, 288);
        
        piano.add(keybut1);
        
        piano.add(blackey1);
        
        piano.add(keybut2);
        
        piano.add(keybut3);
        
        piano.add(keybut4);
        
        piano.add(keybut5);
        
        piano.add(keybut6);
        
        piano.add(keybut7);
        
        piano.add(keybut8);
 
      /*  piano.add(create);
      
        piano.add(play);
        
        piano.add(peredati);
        
        piano.add(priem);
        
        piano.add(stop);
 
        piano.add(r1);
        
        piano.add(r2);
        
        piano.add(r3);*/
 
        setContentPane(piano);
        
        addKeyListener(new KeyAdapter() {
        
            booleanFSoundKey = true;
            
            @Override
            
            public void keyPressed(KeyEventevt) {
            
                int x = 0, y = 0;
                
                switch (evt.getKeyCode()) {
                
                    case KeyEvent.VK_A:
                    
                        if (FSoundKey == true){
                        
                            x = keybut1.getX() + 2;
                            
                            y = keybut1.getY() + 9;
                            
                            keybut1.setLocation(x, y);
                            
                            FSoundKey = false;
                            
                        }
                        
                        break;
                        
                       
                    case KeyEvent.VK_S:
                    
                        if (FSoundKey == true) {
                        
                            x = keybut2.getX() + 2;
                            
                            y = keybut2.getY() + 9;
                            
                            keybut2.setLocation(x, y);
                            
                            FSoundKey = false;
                            
                        }
                        
                        break;
                        
                    case KeyEvent.VK_D:
                    
                        if (FSoundKey == true) {
                        
                            x = keybut3.getX() + 2;
                            
                            y = keybut3.getY() + 9;
                            
                            keybut3.setLocation(x, y);
                            
                            FSoundKey = false;
                            
                        }
                        
                        break;
                        
                    case KeyEvent.VK_F:
                    
                        if (FSoundKey == true) {
                        
                            x = keybut4.getX() + 2;
                            
                            y = keybut4.getY() + 9;
                            
                            keybut4.setLocation(x, y);
                            
                            FSoundKey = false;
                            
                        }
                        
                        break;
                        
                    case KeyEvent.VK_G:
                    
                        if (FSoundKey == true) {
                        
                            x = keybut5.getX() + 2;
                            
                            y = keybut5.getY() + 9;
                            
                            keybut5.setLocation(x, y);
                            
                            FSoundKey = false;
                            
                        }
                        
                        break;
                        
                    case KeyEvent.VK_H:
                   
                        if (FSoundKey == true) {
                        
                            x = keybut6.getX() + 2;
                            
                            y = keybut6.getY() + 9;
                            
                            keybut6.setLocation(x, y);
                            
                            FSoundKey = false;
                            
                        }
                        break;
                        
                    case KeyEvent.VK_J:
                    
                        if (FSoundKey == true) {
                        
                            x = keybut7.getX() + 2;
                            
                            y = keybut7.getY() + 9;
                            
                            keybut7.setLocation(x, y);
                            
                            FSoundKey = false;
                            
                        }
                        
                        break;
                        
                    case KeyEvent.VK_K:
                    
                        if (FSoundKey == true) {
                        
                            x = keybut8.getX() + 2;
                            
                            y = keybut8.getY() + 9;
                            
                            keybut8.setLocation(x, y);
                            
                            FSoundKey = false;
                            
                        }
                        
                        break;
                        
                }
                
            }
            
            @Override
            
            public void keyReleased(KeyEvent e) {
            
                int x = 0, y = 0;
                
                switch (e.getKeyCode()){
                
                    case KeyEvent.VK_A:
                    
                        x = keybut1.getX() - 2;
                        
                        y = keybut1.getY() - 9;
                        
                        keybut1.setLocation(x,y);
                        
                        FSoundKey = true;
                        
                        break;
                        
                    case KeyEvent.VK_S:
                    
                        x = keybut2.getX() - 2;
                        
                        y = keybut2.getY() - 9;
                        
                        keybut2.setLocation(x, y);
                        
                        FSoundKey = true;
                        
                        break;
                        
                    case KeyEvent.VK_D:
                    
                        x = keybut3.getX() - 2;
                        
                        y = keybut3.getY() - 9;
                        
                        keybut3.setLocation(x, y);
                        
                        FSoundKey = true;
                        
                        break;
                        
                    case KeyEvent.VK_F:
                    
                        x = keybut4.getX() - 2;
                        
                        y = keybut4.getY() - 9;
                        
                        keybut4.setLocation(x, y);
                        
                        FSoundKey = true;
                        
                          break;
                          
                    case KeyEvent.VK_G:
                    
                        x = keybut5.getX() - 2;
                        
                        y = keybut5.getY() - 9;
                        
                        keybut5.setLocation(x, y);
                        
                        FSoundKey = true;
                        
                        break;
                        
                    case KeyEvent.VK_H:
                    
                        x = keybut6.getX() - 2;
                        
                        y = keybut6.getY() - 9;
                        
                        keybut6.setLocation(x, y);
                        
                        FSoundKey = true;
                        
                        break;
                        
                    case KeyEvent.VK_J:
                    
                        x = keybut7.getX() - 2;
                        
                        y = keybut7.getY() - 9;
                        
                        keybut7.setLocation(x, y);
                        
                        FSoundKey = true;
                        
                        break;
                        
                    case KeyEvent.VK_K:
                    
                        x = keybut8.getX() - 2;
                        
                        y = keybut8.getY() - 9;
                        
                        keybut8.setLocation(x, y);
                        
                        FSoundKey = true;
                        
                        break;
                }
                
            }
 
        });
    }
}

