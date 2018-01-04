# Plongee
# J'ai peut etre trouver un truc sympa pour inserer un gif dès le lancement de jeu
# J'ai trouvé plusieurs gifs sympa que l'on pourrait utiliser! Je te montrerai ça à la rentrée 

package pkg;
 
import java.awt.BorderLayout;
 
import javax.swing.ImageIcon;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.SwingUtilities;
 
public class TestImage extends JFrame {
	private static final long serialVersionUID = 1L;
 
	public TestImage() {
		super("TestImage");
		setDefaultCloseOperation(EXIT_ON_CLOSE);
 
		getContentPane().add(new JLabel(new ImageIcon(ClassLoader.getSystemResource("pkg/img/loading24.gif"))), BorderLayout.SOUTH);
 
	}
 
	public static void main(String[] args) {
		SwingUtilities.invokeLater(new Runnable() {
			@Override
			public void run() {
				JFrame frame = new TestImage();
				frame.setSize(320, 240);
				frame.setLocationRelativeTo(null);
				frame.setVisible(true);
			}
		});
	}
}
