(
SynthDef(\gabberkick, {
    var snd, low, hi;
    snd = SinOsc.ar(\freq.kr(54) * XLine.kr(5, 1, 0.07) * XLine.kr(1.05, 1, 0.32));
    snd = snd * Env.perc(0.01, 2.0, curve: -8).ar;
    snd = (snd * 40.dbamp).tanh;
    snd = BHiShelf.ar(snd, 200, 1, -8);
    snd = BPeakEQ.ar(snd, \ffreq.kr(1000) * XLine.kr(1, 0.5, 0.5), 1, 15);
    snd = BPeakEQ.ar(snd, \ffreq.kr(1000) * 1.6 * XLine.kr(1, 0.5, 0.5), 1, 8);
    snd = (snd * 6.dbamp).tanh;
    snd = snd + ((snd.sign - snd) * -20.dbamp);
    low = LPF.ar(LPF.ar(snd, 500), 500);
    hi = HPF.ar(HPF.ar(snd, 500), 500);
    hi = DelayC.ar(hi, 0.2, SinOsc.kr(2, [1.5pi, 0.5pi]).range(0, 0.001));
    hi = hi * -3.dbamp;
    snd = low + hi;
    snd = (snd * 60.dbamp).tanh;
    snd = snd * Env.asr(0, 1, 0.01).kr(Done.freeSelf, \gate.kr(1));
    Out.ar(\out.kr(0), snd * \amp.kr(0.1));
}).add;
)

(
Pbind(*[
    instrument: \gabberkick,
    amp: -20.dbamp,
    legato: 0.9,
    dur: Pseq([1, 1, 1, 1, 0.5, 0.5, 1, 0.5, 0.5], inf),
    freq: Pstutter(Pseq([4, 5], inf), Pexprand(40, 100, inf)),
    ffreq: Pstutter(Pseq([4, 5], inf), Pexprand(200, 3000, inf)),
]).play(TempoClock(350 / 60));
)





///// CUSTARD EDIT //////////

(
SynthDef(\gabberkick, {
    var snd, low, hi;
    snd = SinOsc.ar(\freq.kr(54) * MouseX.kr(10, 1, 0.07) * MouseY.kr(1.5, 1, 0.32));
    snd = snd * Env.perc(0.01, 2.0, curve: -8).ar;
    snd = (snd * 40.dbamp).tanh;
    snd = BHiShelf.ar(snd, 200, 1, -8);
    snd = BPeakEQ.ar(snd, \ffreq.kr(1000) * XLine.kr(1, 0.5, 0.5), 1, 15);
    snd = BPeakEQ.ar(snd, \ffreq.kr(1000) * 1.6 * XLine.kr(1, 0.5, 0.5), 1, 8);
    snd = (snd * 6.dbamp).tanh;
    snd = snd + ((snd.sign - snd) * -20.dbamp);
    low = LPF.ar(LPF.ar(snd, 500), 500);
    hi = HPF.ar(HPF.ar(snd, 500), 500);
    hi = DelayC.ar(hi, 0.2, SinOsc.kr(2, [1.5pi, 0.5pi]).range(0, 0.001));
    hi = hi * -3.dbamp;
    snd = low + hi;
    snd = (snd * 60.dbamp).tanh;
    snd = snd * Env.asr(0, 1, 0.01).kr(Done.freeSelf, \gate.kr(1));
    Out.ar(\out.kr(0), snd * \amp.kr(0.1));
}).add;
)

(
Pbind(*[
    instrument: \gabberkick,
    amp: -20.dbamp,
    legato: 0.9,
    dur: Pseq([1, 1, 1, 1, 0.5, 0.5, 1, 0.5, 0.5], inf),
    freq: Pstutter(Pseq([4, 5], inf), Pexprand(40, 100, inf)),
    ffreq: Pstutter(Pseq([4, 5], inf), Pexprand(200, 3000, inf)),
]).play(TempoClock(350 / 60));
)
