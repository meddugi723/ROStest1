IntPtr ptrFailStrOut;

    if (fr_mm_GetRecogFailString(out ptrFailStrOut))
    {
        var recogFailString = Marshal.PtrToStringAuto(ptrFailStrOut);
            
	if (recogFailString != preRecogFailString)
            {
                SetErrorString(recogFailString);
                fr_mm_InitRecogFailString();
                preRecogFailString = string.Empty;
	    }
    }[13:39:43]    


test