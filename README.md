# p0op_Battlefield-4
# UnknownCheats.me
Link - https://www.unknowncheats.me/forum/battlefield-4-a/335946-p0op_bf4-external.html
A file for checking the version of the cheat for Battlefield 4, a "crutch" to turn off if a cheat is detected.
Simple code:


    Version current = Assembly.GetExecutingAssembly().GetName().Version;
                WebClient check = new WebClient();
                Version latest = new Version(check.DownloadString("https://raw.githubusercontent.com/TheOzyUC/Battlefield-4/master/textfile.txt"));
                if (latest > current)
                {
                    DialogResult result = MessageBox.Show(
                   "DETECTED!",
                   "WhoopS'(",
                    MessageBoxButtons.OK,
                    MessageBoxIcon.Information,
                    MessageBoxDefaultButton.Button1,
                    MessageBoxOptions.DefaultDesktopOnly);
     
                    if (result == DialogResult.OK)
     
                    {
                        System.Diagnostics.Process.Start("https://www.unknowncheats.me/forum/battlefield-4-a/335946-p0op_bf4-external.html");
                        
                          //  Environment.Exit(0);
                    }
                }
