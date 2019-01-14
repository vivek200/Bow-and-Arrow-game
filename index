import java.awt.*;
import java.awt.event.KeyEvent;
import java.awt.event.KeyListener;
import java.applet.*;
import javax.swing.JOptionPane;
public class arrow extends Applet implements Runnable,KeyListener{
	Thread t;
	Image ic,id,ie,ig,ic1;
	
	int a=1000,b=1300;int re,inv;   
	
	// score
	double scr=0;
	String sta="Press 's to shoot arrow !";
	String st="Your Score is = ";
	Font f;
	public void init()
	 {
		  f=new Font("Arial",Font.BOLD,20);
		  setFont(f);
		 t=new Thread(this);
		 t.start();
		 ig=getImage(getCodeBase(),"bowcl.png");
		 ic=getImage(getCodeBase(),"baloon.jpg");
		// ic1=getImage(getCodeBase(),"baloon.jpg");
		 id=getImage(getCodeBase(),"artr.jpg");
		 ie=getImage(getCodeBase(),"blueb.png");
		 addKeyListener(this);
	 }
	 public void paint(Graphics g)
	 {
	      
		 g.drawImage(id,b,100,100,90,this);
		 g.drawString(st, 50, 300);
		 g.drawString(sta, 50, 150);
		 if(inv!=1)	 
		 g.drawImage(ic,1200,a,50,150,this);
//		 g.drawImage(ic1,1200,a,50,200,this);
		 if(inv==1)
		 {
			 g.drawImage(ie,1200,a,50,150,this);
		 }
		  if(b>1250)
		 g.drawImage(ig,20,90,120,100,this);
	 }
	 public void run()
	 {try{ while(true)
	 {  
		 a=a-11;
		 
		 if(a<-50)
		 {	 a=1000;  inv=0; }
		 b=b+30;
		 if(b>1250 && re==1)
		 { b=10;   re=0; 
		 }  
		 
		 
		      // because by thread while loop it goes addition of 2 instead of 1
		 st=("Your Score is = "+scr);
		 if(b>1100 && b<1150 && a>60 && a<150)
			 {
			   scr=scr+10;
			   inv=1;  
			 } 
		 Thread.sleep(70);
		 repaint();
	 }
	 }catch(Exception e){}
	 }
	@Override
	public void keyPressed(KeyEvent kp) {
		  if(kp.getKeyChar()=='s' && b>1250)
			    {  sta="";
			  re=1;
			  }
	}
	@Override
	public void keyReleased(KeyEvent arg0) {
		// TODO Auto-generated method stub
		
	}
	@Override
	public void keyTyped(KeyEvent arg0) {
		// TODO Auto-generated method stub
	}

}
